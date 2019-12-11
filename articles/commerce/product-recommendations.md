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
# <a name="product-recommendations-overview"></a><span data-ttu-id="f885c-104">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="f885c-104">Product recommendations overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="f885c-105">Microsoft Dynamics 365 Commerce kann verwendet werden, um Produktempfehlungen auf der E-Commerce-Website und dem POS-Gerät (Point of Sale) anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f885c-105">Microsoft Dynamics 365 Commerce can be used to show product recommendations on the e-Commerce website and point of sale (POS) device.</span></span> <span data-ttu-id="f885c-106">Produktempfehlungen sind Artikel, an denen ein Kunde interessiert sein könnte.</span><span class="sxs-lookup"><span data-stu-id="f885c-106">Product recommendations are items that a customer might be interested in.</span></span> <span data-ttu-id="f885c-107">Die Empfehlungen basieren auf den Kauftrends anderer Kunden in Online- und physischen Filialen.</span><span class="sxs-lookup"><span data-stu-id="f885c-107">The recommendations are based on the purchase trends of other customers in online and brick-and-mortar stores.</span></span>

<span data-ttu-id="f885c-108">Mit Produktempfehlungen können Kunden leicht und schnell die gewünschten Produkte finden, während sie eine Erfahrung erhalten, die ihnen gute Dienste leistet.</span><span class="sxs-lookup"><span data-stu-id="f885c-108">Product recommendations let customers easily and quickly find products that they want while they have an experience that serves them well.</span></span> <span data-ttu-id="f885c-109">Cross-Selling und Upselling können Kunden sogar dabei unterstützen, zusätzliche Produkte zu finden, deren Kauf sie ursprünglich nicht eingeplant hatten.</span><span class="sxs-lookup"><span data-stu-id="f885c-109">Cross-selling and upselling can even be used to help customers find additional products than they didn't originally intend to buy.</span></span> <span data-ttu-id="f885c-110">Wenn Empfehlungen zur Unterstützung der Produktfindung verwendet werden, können sie mehr Conversion-Möglichkeiten schaffen, den Umsatz steigern und sogar die Kundenzufriedenheit und -bindung verbessern.</span><span class="sxs-lookup"><span data-stu-id="f885c-110">When recommendations are used to help with product discovery, they can create more conversion opportunities, help increase sales revenue, and even help enhance customer satisfaction and retention.</span></span>

<span data-ttu-id="f885c-111">In Commerce basieren Produktempfehlungen in großem Umfang auf maschinellen Lerntechnologien von Microsoft Recommendations.</span><span class="sxs-lookup"><span data-stu-id="f885c-111">In Commerce, product recommendations are powered by Microsoft Recommendations machine learning technologies on a large scale.</span></span>


## <a name="scenarios"></a><span data-ttu-id="f885c-112">Szenarien</span><span class="sxs-lookup"><span data-stu-id="f885c-112">Scenarios</span></span>

<span data-ttu-id="f885c-113">Produktempfehlungen sind für die folgenden Szenarien verfügbar:</span><span class="sxs-lookup"><span data-stu-id="f885c-113">Product recommendations are available for the following scenarios:</span></span>

- <span data-ttu-id="f885c-114">**Auf jeder Filialseite zum Durchsuchen oder jeder Landingpage im E-Commerce:** Wenn Kunden oder Geschäftspartner eine Filialseite besuchen, kann die Empfehlungs-Engine Produkte in den Listen **Neu**, **Bestseller** und **Populär** vorschlagen.</span><span class="sxs-lookup"><span data-stu-id="f885c-114">**On any store page for browsing or landing page in e-Commerce:** If customers or store associates visit a store page, the recommendation engine can suggest products in the **New**, **Best Selling**, and **Trending** lists.</span></span>
- <span data-ttu-id="f885c-115">**Auf jeder Produktdetailseite:** Wenn Kunden oder Filialmitarbeiter die Seite **Produktdetails** aufrufen, schlägt die Empfehlungs-Engine zusätzliche Artikel vor, die wahrscheinlich auch gekauft werden.</span><span class="sxs-lookup"><span data-stu-id="f885c-115">**On the Product details page:** If customers or store associates visit a **Product details** page, the recommendation engine suggests additional items that are also likely to be purchased.</span></span> <span data-ttu-id="f885c-116">Diese Artikel werden in der Liste **Personen gefällt auch** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f885c-116">These items appear in the **People also like** list.</span></span>
- <span data-ttu-id="f885c-117">**Auf der Transaktionsseite oder der Auscheckseite:** Die Empfehlungs-Engine schlägt Artikel basierend auf der gesamten Liste der Artikel im Warenkorb vor.</span><span class="sxs-lookup"><span data-stu-id="f885c-117">**On the Transaction page or the checkout page:** The recommendation engine suggests items, based on the whole list of items in the basket.</span></span> <span data-ttu-id="f885c-118">Diese Artikel werden in der Liste **Wird häufig zusammen gekauft** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f885c-118">These items appear in the **Frequently bought together** list.</span></span>

## <a name="recommendation-service"></a><span data-ttu-id="f885c-119">Empfehlungsdienstleistung</span><span class="sxs-lookup"><span data-stu-id="f885c-119">Recommendation service</span></span>

<span data-ttu-id="f885c-120">Produktempfehlungen verwenden die Recommendations-Technologien für maschinelles Lernen auf folgende Weise:</span><span class="sxs-lookup"><span data-stu-id="f885c-120">Product recommendations use the Recommendations machine learning technologies in the following way:</span></span>

- <span data-ttu-id="f885c-121">Daten in dem für den Empfehlungsdienst erforderlichen Format werden aus der Commerce-Betriebsdatenbank extrahiert und an den Entitätsspeicher gesendet.</span><span class="sxs-lookup"><span data-stu-id="f885c-121">Data in the format that the Recommendation service requires is extracted from the Commerce operational database and sent to the Entity store.</span></span>
- <span data-ttu-id="f885c-122">Der Empfehlungsdienst verwendet die Daten, um die Empfehlungsmodule für die Listen **Personen gefällt auch**, **Wird häufig zusammen gekauft**, **Neu**, **Bestseller** und **Populär** zu schulen.</span><span class="sxs-lookup"><span data-stu-id="f885c-122">The Recommendation service uses the data to train recommendation models for the **People also like**, **Frequently bought together**, **New**, **Best selling**, and **Trending** lists.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f885c-123">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f885c-123">Additional resources</span></span>

[<span data-ttu-id="f885c-124">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="f885c-124">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="f885c-125">Erstellen von kuratierten Produktempfehlungslisten</span><span class="sxs-lookup"><span data-stu-id="f885c-125">Create curated product recommendation lists</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="f885c-126">Verwalten von KI-ML-basierten Produktempfehlungsergebnissen</span><span class="sxs-lookup"><span data-stu-id="f885c-126">Manage AI-ML-based product recommendation results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="f885c-127">Hinzufügen von Produktempfehlungslisten zu Seiten</span><span class="sxs-lookup"><span data-stu-id="f885c-127">Add product recommendation lists to pages</span></span>](add-reco-list-to-page.md)
