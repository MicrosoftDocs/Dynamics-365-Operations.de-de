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
ms.openlocfilehash: cf3df2267671b50c20b28dbdb1c6a21696bf2515
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "3664977"
---
# <a name="product-recommendations-faq"></a><span data-ttu-id="e13c3-103">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="e13c3-103">Product recommendations FAQ</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="e13c3-104">Dieses Thema enthält Informationen über die Prozesse und Tools, die Sie verwenden können, um Probleme zu beheben, die den [Produktempfehlungen](product-recommendations.md) oder deren Ergebnisse zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="e13c3-104">This topic provides information about processes and tools that you can use to troubleshoot issues that are related to [product recommendations](product-recommendations.md) or their results.</span></span>

## <a name="best-practices"></a><span data-ttu-id="e13c3-105">Bewährte Methoden</span><span class="sxs-lookup"><span data-stu-id="e13c3-105">Best practices</span></span>
<span data-ttu-id="e13c3-106">Es ist außerordentlich wichtig, das Konzept von Produktmastern und von Varianten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="e13c3-106">It's very important to utilize the concept of product masters and variants.</span></span> <span data-ttu-id="e13c3-107">Die vernünftige Gruppierung von Varianten zu einem übergeordneten Produktmaster hilft dem Listenalgorithmus und erstellt bessere Modelle.</span><span class="sxs-lookup"><span data-stu-id="e13c3-107">The sensible grouping of variants to a parent product master helps the list algorithms and service create better models.</span></span> <span data-ttu-id="e13c3-108">Darüber hinaus kann der Service nur eine Instanz eines Produkts bedienen statt alle eng zugehörigen Varianten in einer Liste zu nutzen.</span><span class="sxs-lookup"><span data-stu-id="e13c3-108">Additionally, the service can serve just one instance of a product instead of putting all closely related variants in a list.</span></span> <span data-ttu-id="e13c3-109">Wenn alle zugehörigen können Varianten in einer Liste verwendet werden, können fehlerhafte oder doppelte Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="e13c3-109">When all closely related variants are put in a list, erroneous or duplicate results can occur.</span></span>

## <a name="why-are-products-missing-from-my-recommendation-lists"></a><span data-ttu-id="e13c3-110">Warum fehlen Produkte aus meinen Empfehlungslisten?</span><span class="sxs-lookup"><span data-stu-id="e13c3-110">Why are products missing from my recommendation lists?</span></span>

<span data-ttu-id="e13c3-111">Normalerweise wenn ein Artikel fehlt in einer Produktempfehlungsliste, ist es ein  Produktkonfigurationsproblem.</span><span class="sxs-lookup"><span data-stu-id="e13c3-111">Typically, if an item is missing from a product recommendation list, there might be a product configuration issue.</span></span> <span data-ttu-id="e13c3-112">Beispielsweise gibt es ein falsches Produktstartdatum oder Enddatum, eine Abmessung ist falsch konfiguriert oder das Produkt ist nicht im richtigen Kanalsortiment, etc.</span><span class="sxs-lookup"><span data-stu-id="e13c3-112">For example, there might be an incorrect product start date or end date, a dimension might be misconfigured, or the product might not be in the correct channel assortment, etc.</span></span>

<span data-ttu-id="e13c3-113">Wenn ein Artikel in einer Empfehlungsliste fehlt, die auf der maschinellen Lernverfahren mit künstlicher Intelligenz (AI-ML) basiert, passt der Artikel möglicherweise nicht die Empfehlungsliste oder es sind möglicherweise nicht genügend Einkaufsbuchungen für die Empfehlungsliste vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e13c3-113">If an item is missing from a recommendation list that is based on artificial intelligence-machine learning (AI-ML), the item might not fit the criteria of the recommendation list, or it might not have enough purchase transactions for the recommendation list to show it.</span></span>

<span data-ttu-id="e13c3-114">Es wird empfohlen, diese Schritte zu prüfen:</span><span class="sxs-lookup"><span data-stu-id="e13c3-114">We recommend that you check these steps:</span></span>
1. <span data-ttu-id="e13c3-115">**Überprüfen Sie, ob in der Produktempfehlungen die Hauptniederlassung aktiviert wurden.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-115">**Make sure that product recommendations have been enabled in HQ.**</span></span> <span data-ttu-id="e13c3-116">Weitere Informationen dazu, wie diese Funktion aktiviert wird, finden Sie unter [Aktivieren von Produktempfehlungen](enable-product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-116">For more information about how to enable this service, see [Enable product recommendations](enable-product-recommendations.md).</span></span>
1. <span data-ttu-id="e13c3-117">**Überprüfen Sie, dass entscheidende Produktattribute festgelegt werden.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-117">**Make sure that key product properties are set.**</span></span> <span data-ttu-id="e13c3-118">Es müssen z.B Sortimente auf **Einschließen** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="e13c3-118">For example, product assortments must be set to **Include**.</span></span>
1. <span data-ttu-id="e13c3-119">**Für neu asssortierte Produkte kann es möglicherweise bis zu 3 Stunden dauern, bevor das Produkt auf der neuen Liste angezeigt wird.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-119">**For newly assorted products, it might take up to 3 hours before the product will start appearing in the new list.**</span></span>
1. <span data-ttu-id="e13c3-120">**Wenn ein Produkt noch immer nicht in Trends, Bestseller, Personen gefällt auch oder werden häufig auch zusammen eingekauft, erscheint, dann hat dieses Produkt nicht genügend Transaktionen.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-120">**If a product is still not appearing in Trending, Best selling, People also like, or Frequently bought together, then that product might not have enough transactions.**</span></span> <span data-ttu-id="e13c3-121">In diesem Fall können Sie entweder auf mehr Transaktionen warten, die Standardempfehlungslistenparameter aktualisieren, oder manuellen Aktivitäten verwenden, um die Empfehlungsproduktlisteergebnisse zu ändern.</span><span class="sxs-lookup"><span data-stu-id="e13c3-121">In this case, you can either wait for more transactions to occur, update the default recommendation list parameters, or use manual intervention to modify the recommendation product list results.</span></span> <span data-ttu-id="e13c3-122">Weitere Informationen zu Empfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-122">For more information about recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
1. <span data-ttu-id="e13c3-123">**Überprüfen Sie, ob das Produkt den Empfehlungskriterien der Liste entspricht.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-123">**Make sure that the product meets the recommendation criteria for the list.**</span></span> <span data-ttu-id="e13c3-124">Weitere Informationen zu Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-124">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="how-can-i-prevent-poor-recommendation-results-from-being-returned"></a><span data-ttu-id="e13c3-125">Wie kann ich schlechte Empfehlungsergebnisse verhindern?</span><span class="sxs-lookup"><span data-stu-id="e13c3-125">How can I prevent poor recommendation results from being returned?</span></span>

<span data-ttu-id="e13c3-126">Empfehlungslisten erfordern eine große Anzahl von Transaktionen, um Ergebnisse zu liefern.</span><span class="sxs-lookup"><span data-stu-id="e13c3-126">Recommendation lists require a large volume of transactions to produce results.</span></span> <span data-ttu-id="e13c3-127">Daher muss klar sein, ob Benutzer vollständige Verlaufs-Buchungsdaten bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="e13c3-127">Therefore, it's important that users provide full historical transaction data.</span></span>

<span data-ttu-id="e13c3-128">Darüber hinaus werden Produkte, die keine Transaktionen oder wenige Transaktionen enthalten haben in der Regel keine **Person gefällt auch** oder **Häufig zusammen gekauft** Ergebnisse und  erscheinen nicht in **Trends** oder **Bestseller-** Empfehlungslisten.</span><span class="sxs-lookup"><span data-stu-id="e13c3-128">Additionally, products that have no transactions or few transactions typically don't have **People also like** or **Frequently bought together** results, and don't appear in **Trending** or **Best selling** recommendation lists.</span></span> <span data-ttu-id="e13c3-129">Diese Situation kann bei sehr neuen Produkte oder für alte Produkten auftreten, die eine geringe Anzahl von Einkäufe haben.</span><span class="sxs-lookup"><span data-stu-id="e13c3-129">This situation can often occur for very new products, or for old products that have a small number of purchases.</span></span> <span data-ttu-id="e13c3-130">Gängige neue Artikel überwinden dieses Problem leicht.</span><span class="sxs-lookup"><span data-stu-id="e13c3-130">Popular new items will easily overcome this issue.</span></span>

<span data-ttu-id="e13c3-131">Es wird empfohlen, diesen Schritten zu folgen:</span><span class="sxs-lookup"><span data-stu-id="e13c3-131">We recommend that you follow these steps:</span></span>
1. <span data-ttu-id="e13c3-132">**Überprüfen Sie, ob das Produkt den Empfehlungskriterien dieser Liste entspricht.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-132">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="e13c3-133">Weitere Informationen zu Produktempfehlungsparameter finden Sie unter AI-ML-basierte Produktempfehlungsergebnisse bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="e13c3-133">For more information about product recommendation parameters, see Modify AI-ML-based product recommendation results.</span></span>
1. <span data-ttu-id="e13c3-134">**Wenn das Produkt neu ist, sollten Sie eine Empfehlungsliste ändern, bis das Produkt mehr Transaktionen aufweist.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-134">**If the product is new, consider modifying a recommendation list until the product has more transactions.**</span></span> <span data-ttu-id="e13c3-135">Weitere Informationen zum Bearbeiten von Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-135">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>


- <span data-ttu-id="e13c3-136">**Überprüfen Sie, ob das Produkt den Empfehlungskriterien dieser Liste entspricht.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-136">**Make sure that the product meets the recommendation criteria for that list.**</span></span> <span data-ttu-id="e13c3-137">Weitere Informationen zu Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-137">For more information about product recommendation parameters, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>
- <span data-ttu-id="e13c3-138">**Wenn das Produkt neu ist, sollten Sie eine Empfehlungsliste ändern, bis das Produkt mehr Transaktionen aufweist.**</span><span class="sxs-lookup"><span data-stu-id="e13c3-138">**If the product is new, consider modifying a recommendation list until the product has more transactions**.</span></span> <span data-ttu-id="e13c3-139">Weitere Informationen zum Bearbeiten von Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-139">For more information about how to modify recommendation list results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

## <a name="can-i-remove-a-product-but-still-see-it-in-the-store"></a><span data-ttu-id="e13c3-140">Kann ich ein Produkt entfernen aber es immer noch im Shop anzeigen?</span><span class="sxs-lookup"><span data-stu-id="e13c3-140">Can I remove a product but still see it in the store?</span></span>

<span data-ttu-id="e13c3-141">Sie können Listen anpassen die algorithmisch generiert werden, wenn eine Geschäftsanforderung entsteht.</span><span class="sxs-lookup"><span data-stu-id="e13c3-141">You can adjust lists that are algorithmically generated if a business need arises.</span></span> <span data-ttu-id="e13c3-142">Wenn ein Produkt aus einer Empfehlungsliste entfernt wird, bleibt das Produkt im Shop auffindbar.</span><span class="sxs-lookup"><span data-stu-id="e13c3-142">However, if a product is removed from a recommendation list, the product will remain discoverable in the store.</span></span> <span data-ttu-id="e13c3-143">Weitere Informationen zum Bearbeiten von Produktempfehlungsparameter finden Sie unter [Verwalten Sie AI-ML-basierte Produktempfehlungsergebnisse](modify-product-recommendation-results.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-143">For more information about how to modify product recommendation results, see [Manage AI-ML-based product recommendation results](modify-product-recommendation-results.md).</span></span>

<span data-ttu-id="e13c3-144">Wenn Sie möchten, dass ein Artikel von Shop nicht angezeigt wird, müssen Die den Wert **Artikelsortiments** auf **ausschließen** ändern.</span><span class="sxs-lookup"><span data-stu-id="e13c3-144">If you must block an item from being discovered in the store, you must change the **Item assortments** value to **Exclude**.</span></span>

## <a name="how-do-i-add-a-list-to-an-e-commerce-page"></a><span data-ttu-id="e13c3-145">Wie wird eine Liste einer E-Commerce-Seite hinzugefügt?</span><span class="sxs-lookup"><span data-stu-id="e13c3-145">How do I add a list to an e-Commerce page?</span></span>

<span data-ttu-id="e13c3-146">Für Informationen dazu, wie Produktempfehlungsseiten Ihrer E-Commerce-Website hinzugefügt werden, finden Sie unter [Produktempfehlungslisten der Seite hinzufügen](add-reco-list-to-page.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-146">For information about how to add product recommendation pages to your e-Commerce website, see [Add product recommendation lists to pages](add-reco-list-to-page.md).</span></span>

## <a name="how-do-i-enable-recommendations-on-pos"></a><span data-ttu-id="e13c3-147">Wie aktiviere ich Empfehlungen für POS?</span><span class="sxs-lookup"><span data-stu-id="e13c3-147">How do I enable recommendations on POS?</span></span>

<span data-ttu-id="e13c3-148">Nachdem Sie Produktempfehlungen aktiviert haben, müssen Sie den Empfehlungsbereich dem Bildschirm der POS-Steuerung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e13c3-148">After enabling product recommendations, you will need to add the recommendations panel to the control POS screen.</span></span> <span data-ttu-id="e13c3-149">Weitere Informationen finden Sie unter [Hinzufügen einer Empfehlungssteuerung zum Transaktionsbild auf POS-Geräten](add-recommendations-control-pos-screen.md).</span><span class="sxs-lookup"><span data-stu-id="e13c3-149">For more information, see [Add a recommendations control to the transaction screen on POS devices](add-recommendations-control-pos-screen.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e13c3-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e13c3-150">Additional resources</span></span>

[<span data-ttu-id="e13c3-151">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="e13c3-151">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="e13c3-152">Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung</span><span class="sxs-lookup"><span data-stu-id="e13c3-152">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="e13c3-153">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="e13c3-153">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="e13c3-154">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="e13c3-154">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="e13c3-155">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="e13c3-155">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="e13c3-156">Die Empfehlungen „Produkte mit ähnlichem Aussehen kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="e13c3-156">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="e13c3-157">Produktempfehlungen in POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e13c3-157">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="e13c3-158">Empfehlungen dem Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e13c3-158">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="e13c3-159">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="e13c3-159">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="e13c3-160">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="e13c3-160">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="e13c3-161">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="e13c3-161">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)
