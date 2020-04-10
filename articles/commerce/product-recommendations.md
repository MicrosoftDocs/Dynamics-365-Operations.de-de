---
title: Überblick über Produktempfehlungen
description: Dieses Thema enthält allgemeine Informationen zu Produktempfehlungen. Mit Produktempfehlungen können Kunden einfach und schnell gesuchte Produkte finden und sogar Produkte, deren Kauf sie ursprünglich nicht eingeplant hatten.
author: Moonma
manager: AnnBe
ms.date: 03/19/2020
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
ms.openlocfilehash: e61136ed296d673e14600762c6f6199093530546
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154225"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="09bac-104">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="09bac-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="09bac-105">Microsoft Dynamics 365 Commerce kann verwendet werden, um Produktempfehlungen auf der E-Commerce-Website und dem POS-Gerät (Point of Sale) anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="09bac-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="09bac-106">Produktempfehlungen sind Artikel, an denen ein Kunde interessiert sein könnte.</span><span class="sxs-lookup"><span data-stu-id="09bac-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="09bac-107">Die Empfehlungen basieren auf den Kauftrends anderer Kunden in Online- und physischen Filialen.</span><span class="sxs-lookup"><span data-stu-id="09bac-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="09bac-108">Mit Produktempfehlungen können Kunden einfach und schnell die gewünschten Produkte finden, während sie eine Erfahrung erhalten, die ihnen gute Dienste leistet.</span><span class="sxs-lookup"><span data-stu-id="09bac-108">Product recommendations allow customers to easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="09bac-109">Cross-Selling und Upselling können Kunden sogar dabei unterstützen, zusätzliche Produkte zu finden, deren Kauf sie ursprünglich nicht eingeplant hatten.</span><span class="sxs-lookup"><span data-stu-id="09bac-109">Cross-selling and upselling can even be used to assist customers find additional products that they didn't originally intend to buy.</span></span> <span data-ttu-id="09bac-110">Wenn Empfehlungen zur Unterstützung der Produktfindung verwendet werden, können sie mehr Conversion-Möglichkeiten schaffen, den Umsatz steigern und sogar die Kundenzufriedenheit und Kundenbindung verbessern.</span><span class="sxs-lookup"><span data-stu-id="09bac-110">When recommendations are used to enhance product discovery, they create more conversion opportunities, help increase sales revenue, and even amplify customer satisfaction and retention.</span></span>

<span data-ttu-id="09bac-111">In E-Commerce basieren Produktempfehlungen in großem Umfang auf maschinellen Lerntechnologien von Microsoft Recommendations.</span><span class="sxs-lookup"><span data-stu-id="09bac-111">In e-Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="09bac-112">Empfehlungsdienstleistung</span><span class="sxs-lookup"><span data-stu-id="09bac-112">Recommendation service</span></span>

<span data-ttu-id="09bac-113">Der Produktempfehlungsdienst verwendet Technologien für künstliche Intelligenz und maschinelles Lernen (AI-ML) auf folgende Weise:</span><span class="sxs-lookup"><span data-stu-id="09bac-113">The product recommendations service utilizes artificial intelligence and machine learning (AI-ML) technologies in the following way:</span></span>

- <span data-ttu-id="09bac-114">Daten in dem für den Empfehlungsdienst erforderlichen Format werden aus der Commerce-Betriebsdatenbank extrahiert und an Azure Data Lake Storage oder den Entitätsspeicher gesendet.</span><span class="sxs-lookup"><span data-stu-id="09bac-114">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to Azure data lake storage (ADLS) or Entity store.</span></span>
- <span data-ttu-id="09bac-115">Der Empfehlungsdienst verwendet die gespeicherten Daten, um die Empfehlungsmodule für die Listen **Personen gefällt auch**, **Wird häufig zusammen gekauft**, **Neu**, **Bestseller** und **Populär** zu schulen.</span><span class="sxs-lookup"><span data-stu-id="09bac-115">The recommendations service uses the stored data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="scenarios"></a><span data-ttu-id="09bac-116">Szenarien</span><span class="sxs-lookup"><span data-stu-id="09bac-116">Scenarios</span></span>

<span data-ttu-id="09bac-117">Produktempfehlungen sind für die folgenden Szenarien verfügbar:</span><span class="sxs-lookup"><span data-stu-id="09bac-117">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="09bac-118">**Auf jeder Filialseite zum Durchsuchen oder jeder Landingpage im E-Commerce:** Wenn Kunden oder Geschäftspartner eine Filialseite besuchen, kann die Empfehlungs-Engine Produkte in den Listen **Neu**, **Bestseller** und **Populär** vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="09bac-118">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="09bac-119">**Auf jeder Produktdetailseite:** Wenn Kunden oder Filialmitarbeiter die Seite **Produktdetails** aufrufen, schlägt die Empfehlungs-Engine zusätzliche Artikel vor, die wahrscheinlich auch gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="09bac-119">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="09bac-120">Diese Artikel werden in der Liste **Personen gefällt auch** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="09bac-120">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="09bac-121">**Auf der Transaktionsseite oder der Auscheckseite:** Die Empfehlungs-Engine schlägt Artikel basierend auf der gesamten Liste der Artikel im Warenkorb vor.</span><span class="sxs-lookup"><span data-stu-id="09bac-121">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="09bac-122">Diese Artikel werden in der Liste **Wird häufig zusammen gekauft** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="09bac-122">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="09bac-123">**Personalisierte Empfehlungen:** Verkaufsberater können angemeldeten Kunden neben neuen Funktionen die personalisierte Liste **Entnahmen für Sie** bieten, mit der vorhandene Listenszenarien basierend auf dem Kunden personalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="09bac-123">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="09bac-124">Um mehr zu erfahren, gehen Sie zu [Personalisierte Empfehlungen aktivieren](personalized-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="09bac-124">To learn more, see [Enable personalized recommendations.](personalized-recommendations.md).</span></span>

### <a name="types-of-product-recommendations"></a><span data-ttu-id="09bac-125">Arten von Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="09bac-125">Types of product recommendations</span></span>

<span data-ttu-id="09bac-126">In der folgenden Tabelle werden verschiedene Arten von automatisierten Produktempfehlungen beschrieben, die Einzelhändlern zur Implementierung in Ihrer Dynamics 365 Commerce Lösung über das [Produktkollektionsmodul](product-collection-module-overview.md) zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="09bac-126">The following table describes various types of automated product recommendations available for retailers to implement in their Dynamics 365 Commerce solution via the [product collection module](product-collection-module-overview.md).</span></span> <span data-ttu-id="09bac-127">Einzelhänder können auch personalisierte Ergebnisse für einen angemeldeten Benutzer anzeigen, wenn der Site-Autor diese Option auswählt.</span><span class="sxs-lookup"><span data-stu-id="09bac-127">Retailers can also show personalized results for a signed-in user if the site author chooses that option.</span></span>

| <span data-ttu-id="09bac-128">Produktsammelmodul</span><span class="sxs-lookup"><span data-stu-id="09bac-128">Product collection module</span></span>  | <span data-ttu-id="09bac-129">Typ</span><span class="sxs-lookup"><span data-stu-id="09bac-129">Type</span></span> | <span data-ttu-id="09bac-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09bac-130">Description</span></span> |
|----------------------------|------|-------------|
| <span data-ttu-id="09bac-131">Neue</span><span class="sxs-lookup"><span data-stu-id="09bac-131">New</span></span>                        | <span data-ttu-id="09bac-132">Algorithmisch</span><span class="sxs-lookup"><span data-stu-id="09bac-132">Algorithmic</span></span> | <span data-ttu-id="09bac-133">Dieses Modul zeigt eine Liste der neuesten Produkte, die kürzlich nach Kanälen und Katalogen sortiert wurden.</span><span class="sxs-lookup"><span data-stu-id="09bac-133">This module shows a list of the newest products that have been recently assorted to channels and catalogs.</span></span> |
| <span data-ttu-id="09bac-134">Bestseller</span><span class="sxs-lookup"><span data-stu-id="09bac-134">Best selling</span></span>               | <span data-ttu-id="09bac-135">Algorithmisch</span><span class="sxs-lookup"><span data-stu-id="09bac-135">Algorithmic</span></span> | <span data-ttu-id="09bac-136">Dieses Modul zeigt eine Liste der Produkte, die nach der höchsten Anzahl an Verkäufen sortiert sind.</span><span class="sxs-lookup"><span data-stu-id="09bac-136">This module shows a list of products that are ranked by the highest number of sales.</span></span> |
| <span data-ttu-id="09bac-137">Populär</span><span class="sxs-lookup"><span data-stu-id="09bac-137">Trending</span></span>                   | <span data-ttu-id="09bac-138">Algorithmisch</span><span class="sxs-lookup"><span data-stu-id="09bac-138">Algorithmic</span></span> | <span data-ttu-id="09bac-139">Dieses Modul zeigt eine Liste der leistungsstärksten Produkte für einen bestimmten Zeitraum an, und zwar geordnet nach der höchsten Anzahl an Verkäufen.</span><span class="sxs-lookup"><span data-stu-id="09bac-139">This module shows a list of the highest-performing products for a given period, ranked by highest number of sales.</span></span>  |
| <span data-ttu-id="09bac-140">Wird häufig zusammen gekauft</span><span class="sxs-lookup"><span data-stu-id="09bac-140">Frequently bought together</span></span> | <span data-ttu-id="09bac-141">AI-ML</span><span class="sxs-lookup"><span data-stu-id="09bac-141">AI-ML</span></span> | <span data-ttu-id="09bac-142">Dieses Modul empfiehlt eine Liste der Produkte, die üblicherweise zusammen mit dem Inhalt des aktuellen Warenkorbs des Verbrauchers gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="09bac-142">This module recommends a list of products that are commonly purchased together with the contents of the consumers current cart.</span></span> |
| <span data-ttu-id="09bac-143">Personen gefällt auch</span><span class="sxs-lookup"><span data-stu-id="09bac-143">People also like</span></span>           | <span data-ttu-id="09bac-144">AI-ML</span><span class="sxs-lookup"><span data-stu-id="09bac-144">AI-ML</span></span> | <span data-ttu-id="09bac-145">Dieses Modul empfiehlt Produkte für ein bestimmtes Saatgutprodukt basierend auf den Kaufmustern der Verbraucher.</span><span class="sxs-lookup"><span data-stu-id="09bac-145">This module recommends products for a given seed product based on consumer purchase patterns.</span></span> |
| <span data-ttu-id="09bac-146">Entnahmen für Sie</span><span class="sxs-lookup"><span data-stu-id="09bac-146">Picks for you</span></span>              | <span data-ttu-id="09bac-147">AI-ML</span><span class="sxs-lookup"><span data-stu-id="09bac-147">AI-ML</span></span> | <span data-ttu-id="09bac-148">Dieses Modul empfiehlt eine personalisierte Liste von Produkten basierend auf den Kaufmustern des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="09bac-148">This module recommends a personalized list of products based on purchase patterns of the signed-in user.</span></span> <span data-ttu-id="09bac-149">Für einen Gastbenutzer wird diese Liste reduziert.</span><span class="sxs-lookup"><span data-stu-id="09bac-149">For a guest user, this list will be collapsed.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="09bac-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="09bac-150">Additional resources</span></span>

[<span data-ttu-id="09bac-151">ADLS in einer Dynamics 365 Commerce-Umgebung aktivieren</span><span class="sxs-lookup"><span data-stu-id="09bac-151">Enable ADLS in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="09bac-152">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="09bac-152">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="09bac-153">Personalisierte Empfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="09bac-153">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="09bac-154">Personalisierte Empfehlungen kündigen</span><span class="sxs-lookup"><span data-stu-id="09bac-154">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="09bac-155">Produktempfehlungen am POS hinzufügen</span><span class="sxs-lookup"><span data-stu-id="09bac-155">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="09bac-156">Empfehlungen zum Transaktionsbildschirm hinzufügen</span><span class="sxs-lookup"><span data-stu-id="09bac-156">Add recommendations to the transaction screen</span></span>](add-recommendations-control-pos-screen.md)

[<span data-ttu-id="09bac-157">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="09bac-157">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="09bac-158">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="09bac-158">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="09bac-159">Empfehlungen mit Demodaten erstellen</span><span class="sxs-lookup"><span data-stu-id="09bac-159">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="09bac-160">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="09bac-160">Product recommendations FAQ</span></span>](faq-recommendations.md)
