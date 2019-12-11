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
# <a name="manage-ai-ml-based-product-recommendation-results"></a><span data-ttu-id="14de7-103">Verwalten von KI-ML-basierten Produktempfehlungsergebnissen</span><span class="sxs-lookup"><span data-stu-id="14de7-103">Manage AI-ML-based product recommendation results</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="14de7-104">In diesem Thema wird erläutert, wie Sie Ergebnisse zu Produktempfehlungen basierend auf maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) an Ihr Unternehmen anpassen.</span><span class="sxs-lookup"><span data-stu-id="14de7-104">This topic explains how to tailor product recommendation results based on artificial intelligence-machine learning (AI-ML) to your business.</span></span> 

<span data-ttu-id="14de7-105">Nach dem Aktivieren der Produktempfehlungen werden die Standardeinstellungen wirksam. Diese Parameter können für viele Anforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14de7-105">After enabling product recommendations, the default settings will take effect; these parameters will work for may work for many needs.</span></span> <span data-ttu-id="14de7-106">Es empfiehlt sich, einige Zeit zum Bewerten einzuplanen und festzustellen, ob die Ergebnisse zur Verkaufsbewegung von Produkten passen.</span><span class="sxs-lookup"><span data-stu-id="14de7-106">It is best to plan to spend some time evaluating whether the results fit the selling motion of products.</span></span> <span data-ttu-id="14de7-107">Wir empfehlen, die Ergebnisse einige Tage lang auszuwerten, bevor Sie die Parameter nach Bedarf ändern und erneut testen.</span><span class="sxs-lookup"><span data-stu-id="14de7-107">We suggest evaluating results for a few days before changing parameters as needed before testing again.</span></span> 

## <a name="understanding-recommendation-list-parameters"></a><span data-ttu-id="14de7-108">Verstehen der Empfehlungslistenparameter</span><span class="sxs-lookup"><span data-stu-id="14de7-108">Understanding recommendation list parameters</span></span>

<span data-ttu-id="14de7-109">Informieren Sie sich vor dem Ändern der Parameter, wie sich diese auf die folgenden Ergebnisse auswirken.</span><span class="sxs-lookup"><span data-stu-id="14de7-109">Before changing the parameters, learn about how they will affect the results below.</span></span>

### <a name="trending-product-list"></a><span data-ttu-id="14de7-110">Populäre Produktliste</span><span class="sxs-lookup"><span data-stu-id="14de7-110">Trending product list</span></span>

<span data-ttu-id="14de7-111">Die **populäre** Produktliste besitzt zwei Parameter, die geändert werden können: ![Beispiel für populäre Standardlistenparameter](./media/exampletrendingparameters.png)</span><span class="sxs-lookup"><span data-stu-id="14de7-111">The **Trending** product list has two parameters that can be changed: ![Example Trending list default parameters](./media/exampletrendingparameters.png)</span></span>
1. <span data-ttu-id="14de7-112">**Neue Produkte aus den letzten X Tagen einbeziehen** – Produkte, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum hinzugefügt wurden, können zur Auswahl von Produktkandidaten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14de7-112">**Include new products from last X days** - Products that have been added within the specified number of days before the current date can be used to select product candidates.</span></span> <span data-ttu-id="14de7-113">Der Standardwert in der Abbildung weist darauf hin, dass Produkte mit einem Alter von 180 Tagen in der Liste der populären Produktliste verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="14de7-113">The default value in the picture suggests that products as old has 180 days can be used in the trending product list.</span></span>
1. <span data-ttu-id="14de7-114">**Verkäufe aus den letzten X Tagen einbeziehen** – Verkaufsvorgänge, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum getätigt wurden, können zum Bestellen der Produkte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14de7-114">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="14de7-115">Der obige Standardwert legt nahe, dass alle Einkäufe, die in den letzten 30 Tagen für ein Produkt getätigt wurden, verwendet werden, um die Platzierung des Produkts in der Liste der populären Produkte zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="14de7-115">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the trending product list.</span></span> 

### <a name="best-selling-product-list"></a><span data-ttu-id="14de7-116">Bestseller-Produktliste</span><span class="sxs-lookup"><span data-stu-id="14de7-116">Best selling product list</span></span>

<span data-ttu-id="14de7-117">Abhängig von Ihrem Unternehmen kann Bestseller andere Ergebnisse als Trends liefern, obwohl beide Transaktionsdaten für die Bestellung von Produkten verwenden.</span><span class="sxs-lookup"><span data-stu-id="14de7-117">Depending on your business, Best selling can bring different results than trending, even though they both use transaction data to order products.</span></span> <span data-ttu-id="14de7-118">Da Bestseller nicht nach Sortimentsdatum ablaufen, können mit Bestseller immer noch sehr beliebte ältere Produkte hervorgehoben werden, die möglicherweise von der Trendliste gestrichen wurden.</span><span class="sxs-lookup"><span data-stu-id="14de7-118">Because best selling has no cut off based on assortment date, Best selling can still highlight very popular, older products that might have been dropped from the trending list.</span></span> 

<span data-ttu-id="14de7-119">Die **Bestseller**-Produktliste besitzt einen Parameter, der geändert werden kann:</span><span class="sxs-lookup"><span data-stu-id="14de7-119">The **Best selling** product list has one parameter that can be changed:</span></span>

![Beispiel für Bestseller-Standardlistenparameter](./media/examplebestsellingparameters.PNG)
1. <span data-ttu-id="14de7-121">**Verkäufe aus den letzten X Tagen einbeziehen** – Verkaufsvorgänge, die innerhalb der angegebenen Anzahl von Tagen vor dem aktuellen Datum getätigt wurden, können zum Bestellen der Produkte verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="14de7-121">**Include sales from last X days** - Sales transactions that have occurred within the specified number of days before the current date can be used to order the products.</span></span> <span data-ttu-id="14de7-122">Der obige Standardwert legt nahe, dass alle Einkäufe, die in den letzten 30 Tagen für ein Produkt getätigt wurden, verwendet werden, um die Platzierung des Produkts in der Bestseller-Produktliste zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="14de7-122">The default value above suggests that all purchases made of a product in the last 30 days would be used to determine the placement of the product in the Best selling product list.</span></span> 

## <a name="manually-add-or-remove-products-from-recommendation-lists"></a><span data-ttu-id="14de7-123">Manuelles Hinzufügen oder Entfernen von Produkten aus Empfehlungslisten</span><span class="sxs-lookup"><span data-stu-id="14de7-123">Manually add or remove products from recommendation lists</span></span>

### <a name="for-new-trending-or-best-selling"></a><span data-ttu-id="14de7-124">Für Neu, Beliebt oder Bestseller</span><span class="sxs-lookup"><span data-stu-id="14de7-124">For New, Trending, or Best selling</span></span>

1.  <span data-ttu-id="14de7-125">Gehen Sie zu **Einzelhandel** > **Produktempfehlungen** > **Empfehlungsparameter**.</span><span class="sxs-lookup"><span data-stu-id="14de7-125">Go to **Retail** > **Product recommendations** > **Recommendation parameters**.</span></span>
1.  <span data-ttu-id="14de7-126">In der Liste mit freigegebenen Einzelhandelsparametern, wählen Sie **Empfehlungslisten** aus.</span><span class="sxs-lookup"><span data-stu-id="14de7-126">In the list of retail shared parameters, select **Recommendation lists**.</span></span>
1.  <span data-ttu-id="14de7-127">Wählen Sie die Liste aus, über die Sie Produkte hinzufügen oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="14de7-127">Select the list add or remove products from.</span></span>
1.  <span data-ttu-id="14de7-128">Um der Tabelle Produkte hinzuzufügen, wählen Sie **Zeile hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="14de7-128">To add products to the table, select **Add line.**</span></span> 
1.  <span data-ttu-id="14de7-129">Suchen Sie in der Spalte Produkte anhand von **Name** oder **Produktnummer** nach einem Produkt.
![Beispiel zur Suche nach einem Produkt in der neuen Produktliste](./media/examplenewlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="14de7-129">Under the Product column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the New product list](./media/examplenewlistconfiguration1.png)</span></span>
1.  <span data-ttu-id="14de7-130">Wählen Sie unter der Spalte Zeilentyp eine von zwei Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="14de7-130">Under the Line type column, select one of two options:</span></span>
    -   <span data-ttu-id="14de7-131">**Einschließen** – rückt ein Produkt an die Spitze der Liste</span><span class="sxs-lookup"><span data-stu-id="14de7-131">**Include** – forces a product to the front of the list</span></span>
    -   <span data-ttu-id="14de7-132">**Ausschließen** – entfernt ein Produkt aus der Liste ![Beispiele für Einschließen oder Ausschließen eines Produktes aus der neuen Produktliste](./media/examplenewlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="14de7-132">**Exclude** – removes a product from appearing in the list ![Example of Including or Excluding a product from the New product list](./media/examplenewlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="14de7-133">Durch das Ändern der **Anzeigereihenfolge** wird die Reihenfolge der Produkte mit der Markierung **Einschließen** in der Liste ändern.</span><span class="sxs-lookup"><span data-stu-id="14de7-133">Changing the **Display order** will change the order that products marked **include** will appear in the list.</span></span>
    - <span data-ttu-id="14de7-134">Wenn zwei Produkte denselben Wert für **Anzeigereihenfolge** besitzen, dann kann die endgültige Reihenfolge dieser beiden Ergebnisse vom Backoffice abweichen.</span><span class="sxs-lookup"><span data-stu-id="14de7-134">If two products have the same **display order** value, then the final order of those two results may differ from the back office.</span></span>
1.  <span data-ttu-id="14de7-135">So entfernen Sie Produkte aus der Tabelle: Wählen Sie die zu entfernende Zeile und dann **Entfernen** aus.</span><span class="sxs-lookup"><span data-stu-id="14de7-135">To remove products from the table: select the line to remove and select **Remove**.</span></span>


### <a name="for-people-also-like-or-frequently-bought-together-lists"></a><span data-ttu-id="14de7-136">Für Listen wie Personen gefällt auch oder Wird häufig zusammen gekauft</span><span class="sxs-lookup"><span data-stu-id="14de7-136">For People also like or Frequently bought together lists</span></span>

<span data-ttu-id="14de7-137">Im Kontext von Listen wie **Wird häufig zusammen gekauft** oder **Personen gefällt auch** wird das maschinelle Lernen verwendet, um die Kaufmuster von Verbrauchern zu analysieren und so verwandte Produkte zu empfehlen, die gemeinsam für ein einzigartiges Startprodukt gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="14de7-137">In the context of **Frequently bought together** or **People also like** lists, machine learning is used to analyze consumer purchase patterns to recommend related products commonly purchased together for a unique seed product.</span></span> 
 
<span data-ttu-id="14de7-138">Ein **Startprodukt** ist das Produkt, für das Sie Ergebnisse generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="14de7-138">A **seed product** is the product you want to generate results for.</span></span> <span data-ttu-id="14de7-139">Im Rahmen der manuellen Anpassung von Empfehlungslisten fügen Sie Ergebnisse für dieses Produkt hinzu oder entfernen sie.</span><span class="sxs-lookup"><span data-stu-id="14de7-139">In the context of manually adjusting recommendation lists, you are adding or removing results for this product.</span></span> 

<span data-ttu-id="14de7-140">Befolgen Sie diese Schritte, um manuell Ergebnisse für ein Startprodukt hinzuzufügen oder zu entfernen:</span><span class="sxs-lookup"><span data-stu-id="14de7-140">Follow these steps to manually add or remove results for a seed product:</span></span>
1.  <span data-ttu-id="14de7-141">Wählen Sie das **Startprodukt** aus.</span><span class="sxs-lookup"><span data-stu-id="14de7-141">Select the **Seed product**.</span></span> 
1.  <span data-ttu-id="14de7-142">Suchen Sie in der Spalte **Produkt** anhand von **Name** oder **Produktnummer** nach einem Produkt.
![Beispiel für die Suche nach einem Produkt in der Liste Wird häufig zusammen gekauft](./media/exampleFBTlistconfiguration1.png)</span><span class="sxs-lookup"><span data-stu-id="14de7-142">Under the **Product** column, search for a product by **Name** or **Product number.**
![Example of searching for a product on the Frequently bought together list](./media/exampleFBTlistconfiguration1.png)</span></span>
1. <span data-ttu-id="14de7-143">Wählen Sie in der Spalte **Zeilentyp** eine von zwei Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="14de7-143">Under the **Line type** column, select one of two options:</span></span>
    - <span data-ttu-id="14de7-144">**Einschließen** – rückt ein Produkt an die Spitze der Liste</span><span class="sxs-lookup"><span data-stu-id="14de7-144">**Include** – forces a product to the front of the list</span></span>
    - <span data-ttu-id="14de7-145">**Ausschließen** – Entfernt ein Produkt aus der Liste</span><span class="sxs-lookup"><span data-stu-id="14de7-145">**Exclude** – removes a product from appearing in the list</span></span>     
<span data-ttu-id="14de7-146">![Beispiel für das Einbeziehen oder Ausschließen eines Produkts in die Liste Wird häufig zusammen gekauft](./media/exampleFBTlistconfiguration2.png)</span><span class="sxs-lookup"><span data-stu-id="14de7-146">![Example of Including or Excluding a product on the Frequently bought together list](./media/exampleFBTlistconfiguration2.png)</span></span>
1.  <span data-ttu-id="14de7-147">So entfernen Sie Produkte aus der Tabelle: Wählen Sie die zu entfernende Zeile und dann Entfernen aus.</span><span class="sxs-lookup"><span data-stu-id="14de7-147">To remove products from the table: select the line to remove and select Remove.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="14de7-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="14de7-148">Additional resources</span></span>

[<span data-ttu-id="14de7-149">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="14de7-149">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="14de7-150">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="14de7-150">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="14de7-151">Hinzufügen von Produktempfehlungslisten zu Seiten</span><span class="sxs-lookup"><span data-stu-id="14de7-151">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
