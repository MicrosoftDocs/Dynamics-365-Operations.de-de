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
ms.openlocfilehash: e249c7d450510a3a9a33158e9e1c33f832a1f91c
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024978"
---
# <a name="product-recommendations-overview"></a><span data-ttu-id="7878f-104">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="7878f-104">Product recommendations overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="7878f-105">Microsoft Dynamics 365 Commerce kann verwendet werden, um Produktempfehlungen auf der E-Commerce-Website und dem POS-Gerät (Point of Sale) anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="7878f-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="7878f-106">Produktempfehlungen sind Artikel, an denen ein Kunde interessiert sein könnte.</span><span class="sxs-lookup"><span data-stu-id="7878f-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="7878f-107">Die Empfehlungen basieren auf den Kauftrends anderer Kunden in Online- und physischen Filialen.</span><span class="sxs-lookup"><span data-stu-id="7878f-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="7878f-108">Mit Produktempfehlungen können Kunden leicht und schnell die gewünschten Produkte finden, während sie eine Erfahrung erhalten, die ihnen gute Dienste leistet.</span><span class="sxs-lookup"><span data-stu-id="7878f-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="7878f-109">Cross-Selling und Upselling können Kunden sogar dabei unterstützen, zusätzliche Produkte zu finden, deren Kauf sie ursprünglich nicht eingeplant hatten.</span><span class="sxs-lookup"><span data-stu-id="7878f-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="7878f-110">Wenn Empfehlungen zur Unterstützung der Produktfindung verwendet werden, können sie mehr Conversion-Möglichkeiten schaffen, den Umsatz steigern und sogar die Kundenzufriedenheit und -bindung verbessern.</span><span class="sxs-lookup"><span data-stu-id="7878f-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="7878f-111">In Commerce basieren Produktempfehlungen in großem Umfang auf maschinellen Lerntechnologien von Microsoft Recommendations.</span><span class="sxs-lookup"><span data-stu-id="7878f-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="7878f-112">Szenarien</span><span class="sxs-lookup"><span data-stu-id="7878f-112">Scenarios</span></span>

<span data-ttu-id="7878f-113">Produktempfehlungen sind für die folgenden Szenarien verfügbar:</span><span class="sxs-lookup"><span data-stu-id="7878f-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="7878f-114">**Auf jeder Filialseite zum Durchsuchen oder jeder Landingpage im E-Commerce:** Wenn Kunden oder Geschäftspartner eine Filialseite besuchen, kann die Empfehlungs-Engine Produkte in den Listen **Neu**, **Bestseller** und **Populär** vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="7878f-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="7878f-115">**Auf jeder Produktdetailseite:** Wenn Kunden oder Filialmitarbeiter die Seite **Produktdetails** aufrufen, schlägt die Empfehlungs-Engine zusätzliche Artikel vor, die wahrscheinlich auch gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="7878f-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="7878f-116">Diese Artikel werden in der Liste **Personen gefällt auch** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7878f-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="7878f-117">**Auf der Transaktionsseite oder der Auscheckseite:** Die Empfehlungs-Engine schlägt Artikel basierend auf der gesamten Liste der Artikel im Warenkorb vor.</span><span class="sxs-lookup"><span data-stu-id="7878f-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="7878f-118">Diese Artikel werden in der Liste **Wird häufig zusammen gekauft** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7878f-118">These items appear in the **Frequently bought together** list.</span></span>
- <span data-ttu-id="7878f-119">**Personalisierte Empfehlungen:** Verkaufsberater können angemeldeten Kunden neben neuen Funktionen die personalisierte Liste **Entnahmen für Sie** bieten, mit der vorhandene Listenszenarien basierend auf dem Kunden personalisiert werden können.</span><span class="sxs-lookup"><span data-stu-id="7878f-119">**Personalized recommendations:** Merchandizers can provide signed-in customers a personalized **picks for you** list, in addition to new functionality that allows for existing list scenarios to be personalized based on that customer.</span></span> <span data-ttu-id="7878f-120">Weitere Informationen finden Sie in der Funktionsdokumentation: [Personalisierte Produktempfehlungen aktivieren.](personalized-recommendations.md)</span><span class="sxs-lookup"><span data-stu-id="7878f-120">To learn more, please see the feature documenation: [enable personalized recommedations.](personalized-recommendations.md)</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="7878f-121">Empfehlungsdienstleistung</span><span class="sxs-lookup"><span data-stu-id="7878f-121">Recommendation service</span></span>

<span data-ttu-id="7878f-122">Produktempfehlungen verwenden die Recommendations-Technologien für maschinelles Lernen auf folgende Weise:</span><span class="sxs-lookup"><span data-stu-id="7878f-122">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="7878f-123">Daten in dem für den Empfehlungsdienst erforderlichen Format werden aus der Commerce-Betriebsdatenbank extrahiert und an den Entitätsspeicher gesendet.</span><span class="sxs-lookup"><span data-stu-id="7878f-123">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="7878f-124">Der Empfehlungsdienst verwendet die Daten, um die Empfehlungsmodule für die Listen **Personen gefällt auch**, **Wird häufig zusammen gekauft**, **Neu**, **Bestseller** und **Populär** zu schulen.</span><span class="sxs-lookup"><span data-stu-id="7878f-124">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7878f-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7878f-125">Additional resources</span></span>

[<span data-ttu-id="7878f-126">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="7878f-126">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="7878f-127">Personalisierte Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="7878f-127">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="7878f-128">Übersicht über Produktsammelmodule</span><span class="sxs-lookup"><span data-stu-id="7878f-128">Product collection module overview</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="7878f-129">Erstellen von kuratierten Produktempfehlungslisten</span><span class="sxs-lookup"><span data-stu-id="7878f-129">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="7878f-130">Verwalten von KI-ML-basierten Produktempfehlungsergebnissen</span><span class="sxs-lookup"><span data-stu-id="7878f-130">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="7878f-131">Hinzufügen von Produktempfehlungslisten zu Seiten</span><span class="sxs-lookup"><span data-stu-id="7878f-131">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
