---
title: Übersicht der Produktdetailseiten
description: Dieses Thema bietet eine Übersicht über Produktdetailseiten (PDPs) in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e4a61383c790b63aa1c07f7004f264495171441a
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792218"
---
# <a name="product-details-pages-overview"></a><span data-ttu-id="4801c-103">Übersicht zu Produktdetailseiten</span><span class="sxs-lookup"><span data-stu-id="4801c-103">Product details pages overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="4801c-104">Dieses Thema bietet eine Übersicht über Produktdetailseiten (PDPs) in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="4801c-104">This topic provides an overview of product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="4801c-105">Eine PDP bietet detaillierte Informationen zu einem Produkt und ermöglicht es Kunden, Produktoptionen wie Größe, Stil und Farbe auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="4801c-105">A PDP provides detailed information about a product, and lets customers select product options such as a size, style, and color.</span></span> <span data-ttu-id="4801c-106">Eine PDP sollte alle Produktinformationen enthalten, die ein Kunde benötigt, um eine Kaufentscheidung zu treffen.</span><span class="sxs-lookup"><span data-stu-id="4801c-106">A PDP should showcase all the product information that a customer requires to make a purchase decision.</span></span>

<span data-ttu-id="4801c-107">Die folgende Abbildung zeigt ein Beispiel für eine PDP.</span><span class="sxs-lookup"><span data-stu-id="4801c-107">The following illustration shows an example of a PDP.</span></span>

![Beispiel einer Produktdetailseite](./media/pdp.PNG)

## <a name="header-and-footer-modules"></a><span data-ttu-id="4801c-109">Kopf- und Fußzeilenmodule</span><span class="sxs-lookup"><span data-stu-id="4801c-109">Header and footer modules</span></span>

<span data-ttu-id="4801c-110">Oben in der PDP befindet sich eine Kopfzeile mit allen Produktkategorien und anderen Seiten, die Kunden auf Wunsch des Einzelhändlers durchsuchen sollen.</span><span class="sxs-lookup"><span data-stu-id="4801c-110">The top of a PDP has a header that shows all the product categories and other pages that the retailer wants customers to browse.</span></span> <span data-ttu-id="4801c-111">Unten in der Seite befindet sich eine Fußzeile mit Direktlinks zu verschiedenen Themen, die Kunden interessieren könnten.</span><span class="sxs-lookup"><span data-stu-id="4801c-111">The bottom of the page has a footer that contains quick links to various topics that might interest customers.</span></span>

## <a name="buy-box-module"></a><span data-ttu-id="4801c-112">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="4801c-112">Buy box module</span></span>

<span data-ttu-id="4801c-113">Das wichtigste Modul auf einer PDP ist das Kauffeldmodul, das als erstes Element im Hauptabschnitt der Seite angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="4801c-113">The most important module on a PDP is the buy box module, which appears as the first item in the main section of the page.</span></span> <span data-ttu-id="4801c-114">Ein Kauffeldmodul zeigt wichtige Produktinformationen wie den Produktnamen, die Produktbeschreibung, den Produktpreis, Produktbilder und Produktbewertungen an.</span><span class="sxs-lookup"><span data-stu-id="4801c-114">A buy box module shows important product information, such as the product name, the product description, the product price, product images, and product ratings.</span></span>

<span data-ttu-id="4801c-115">Mit dem Kauffeldmodul kann der Kunde Produktoptionen (z. B. Größe, Stil und Farbe) auswählen und das Produkt in den Einkaufskorb legen.</span><span class="sxs-lookup"><span data-stu-id="4801c-115">The buy box module lets the customer select product options (for example, a size, style, and color) and add the product to the cart.</span></span> <span data-ttu-id="4801c-116">Der Kunde kann das Produkt auch online kaufen und in einem Geschäft abholen.</span><span class="sxs-lookup"><span data-stu-id="4801c-116">It also lets the customer buy the product online and pick it up in a store.</span></span> <span data-ttu-id="4801c-117">Das Modul Online kaufen und im Geschäft abholen verwendet die Integration mit Bing Maps-APIs (Application Programming Interfaces), um Geschäfte in der Nähe oder Geschäfte an einem anderen vom Kunden angegebenen Ort zu finden.</span><span class="sxs-lookup"><span data-stu-id="4801c-117">The buy online and pick up in store module uses integration with Bing Maps application programming interfaces (APIs) to find nearby stores or stores in another location that the customer specifies.</span></span>

<span data-ttu-id="4801c-118">Ein Kauffeldmodul erfordert eine Produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="4801c-118">A buy box module requires a product ID.</span></span> <span data-ttu-id="4801c-119">Diese ID wird aus dem Seitenkontext abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="4801c-119">This ID is derived from the page context.</span></span> <span data-ttu-id="4801c-120">Wenn einer Seite, deren Seitenkontext keine Produkt-ID enthält, ein Kauffeldmodul hinzugefügt wird, werden die Informationen nicht korrekt wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="4801c-120">If a buy box module is added to a page where the page context doesn't include a product ID, it won't render the information correctly.</span></span>

## <a name="product-specifications-module"></a><span data-ttu-id="4801c-121">Produktklassifizierungsmodul</span><span class="sxs-lookup"><span data-stu-id="4801c-121">Product specifications module</span></span>

<span data-ttu-id="4801c-122">Mit dem Produktklassifizierungsmodul können zusätzliche Details zum Produkt angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4801c-122">The product specifications module can be used to showcase additional details about the product.</span></span> <span data-ttu-id="4801c-123">Diese Details werden aus den Produktattributen in Commerce übernommen.</span><span class="sxs-lookup"><span data-stu-id="4801c-123">These details are taken from product attributes in Commerce.</span></span> <span data-ttu-id="4801c-124">Das Produktklassifizierungsmodul zeigt jedes Attribut, bei dem die Eigenschaft **sichtbar** auf **true** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="4801c-124">The product specifications module shows every attribute where the **visible** property is set to **true**.</span></span> <span data-ttu-id="4801c-125">Es erfordert eine Produkt-ID, um die Produktattribute abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4801c-125">It requires a product ID to retrieve the product attributes.</span></span>

## <a name="recommendations-module"></a><span data-ttu-id="4801c-126">Empfehlungsmodul</span><span class="sxs-lookup"><span data-stu-id="4801c-126">Recommendations module</span></span>

<span data-ttu-id="4801c-127">Das Empfehlungsmodul ist ein wichtiges Modul auf einer PDP.</span><span class="sxs-lookup"><span data-stu-id="4801c-127">The recommendations module is an important module on a PDP.</span></span> <span data-ttu-id="4801c-128">Während Kunden nach Produkten suchen, sollten ihnen mehr Produktoptionen angeboten werden, damit sie das richtige Produkt finden und einen Kauf tätigen können.</span><span class="sxs-lookup"><span data-stu-id="4801c-128">While customers browse for products, more product options should be presented to them, so that they can find the correct product and make a purchase.</span></span> <span data-ttu-id="4801c-129">Mithilfe von Empfehlungen können Kunden auf einfache Weise verwandte Inhalte entdecken und weiter einkaufen.</span><span class="sxs-lookup"><span data-stu-id="4801c-129">Recommendations help customers easily discover related content and continue to shop.</span></span>

<span data-ttu-id="4801c-130">Es gibt verschiedene Arten von Empfehlungslisten:</span><span class="sxs-lookup"><span data-stu-id="4801c-130">Different types of recommendation lists are available:</span></span>

- <span data-ttu-id="4801c-131">Die Liste **Personen gefällt auch** basiert auf dem maschinellen Lernen.</span><span class="sxs-lookup"><span data-stu-id="4801c-131">The **People also like** list is based on machine learning.</span></span> <span data-ttu-id="4801c-132">Sie verwendet die Transaktionshistorie anderer Kunden, um Empfehlungen abzugeben.</span><span class="sxs-lookup"><span data-stu-id="4801c-132">It uses the transaction history of other customers to provide recommendations.</span></span> <span data-ttu-id="4801c-133">Diese Liste wird vom Empfehlungsdienst erstellt und ähnelt den Listen „Kunden, die dies gekauft haben, kauften auch ...“.</span><span class="sxs-lookup"><span data-stu-id="4801c-133">This list is generated by the recommendations service and resembles "Customers who bought this also bought..." lists.</span></span> <span data-ttu-id="4801c-134">Eine Produkt-ID ist zum Generieren dieser Liste erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4801c-134">A product ID is required to generate this list.</span></span>
- <span data-ttu-id="4801c-135">Die Liste **Zugehörig** kann für ein Produkt in Commerce konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4801c-135">A **Related** list can be configured for a product in Commerce.</span></span> <span data-ttu-id="4801c-136">Beispielsweise können für eine braune Lederreisehandtasche mehrere Handtaschen auf Lederbasis oder für Reisezwecke entworfene Handtaschen für die Themenliste konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4801c-136">For example, for a brown leather travel handbag, more handbags that are leather-based or designed for travel purposes can be configured for the related list.</span></span> <span data-ttu-id="4801c-137">Andere Typen zugehöriger Listen, wie **Zubehör** und **Weitere ähnliche Aktivitäten**, können auch in Commerce konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4801c-137">Other types of related lists, such as **Accessories** and **More like this**, can also be configured in Commerce.</span></span> <span data-ttu-id="4801c-138">Eine Produkt-ID ist zum Generieren dieser Liste erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4801c-138">A product ID is required to generate this list.</span></span> <span data-ttu-id="4801c-139">Daher ist die Liste leer, wenn sie zu einer Startseite hinzugefügt wird, auf der der Seitenkontext keine Produkt-ID enthält.</span><span class="sxs-lookup"><span data-stu-id="4801c-139">Therefore, if it's added to a home page, where the page context doesn't include a product ID, the list will be empty.</span></span>
- <span data-ttu-id="4801c-140">Algorithmisch generierte Empfehlungslisten, wie **Populär**, **Bestseller** und **Neu** können in PDPs verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4801c-140">Algorithmically generated recommendation lists, such as **Trending**, **Best Selling**, and **New**, can be used on PDPs.</span></span> <span data-ttu-id="4801c-141">Diese Listen stehen zwar möglicherweise nicht in direktem Zusammenhang mit dem Produkt auf der PDP, sind jedoch eine weitere Möglichkeit, Kunden bei der Suche nach Produkten zu unterstützen, die sie interessieren könnten.</span><span class="sxs-lookup"><span data-stu-id="4801c-141">Although these lists might not be directly related to the product on the PDP, they are another way to help customers find products that might interest them.</span></span> <span data-ttu-id="4801c-142">Diese Listentypen erfordern keine Produkt-ID.</span><span class="sxs-lookup"><span data-stu-id="4801c-142">These types of lists don't require a product ID.</span></span> <span data-ttu-id="4801c-143">Hierbei handelt es sich um generische Listen, die auf der Grundlage von Einkaufsmustern auf der gesamten Website erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="4801c-143">They are generic lists that are generated based on shopping patterns across the site.</span></span>
- <span data-ttu-id="4801c-144">Redaktionslisten sind manuell kuratierte Listen.</span><span class="sxs-lookup"><span data-stu-id="4801c-144">Editorial lists are manually curated lists.</span></span> <span data-ttu-id="4801c-145">Beispielsweise kann ein Einzelhändler entscheiden, Listen von Produkten, die präsentiert werden sollen, manuell zu kuratieren.</span><span class="sxs-lookup"><span data-stu-id="4801c-145">For example, a retailer might decide to manually curate lists of products that it wants to showcase.</span></span>

## <a name="ratings-and-reviews-modules"></a><span data-ttu-id="4801c-146">Bewertungs- und Prüfungsmodule</span><span class="sxs-lookup"><span data-stu-id="4801c-146">Ratings and reviews modules</span></span>

<span data-ttu-id="4801c-147">Mit drei Modulen können Prüfungen angezeigt und hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="4801c-147">Three modules can be used to show and add reviews:</span></span>

- <span data-ttu-id="4801c-148">**Prüfungen** – Dieses Modul zeigt Bewertungen und Prüfungen an, die von anderen Kunden bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4801c-148">**Reviews** – This module lists ratings and reviews that have been provided by other customers.</span></span> <span data-ttu-id="4801c-149">Kunden können die Prüfungen sortieren und filtern.</span><span class="sxs-lookup"><span data-stu-id="4801c-149">Customers can sort and filter the reviews.</span></span> <span data-ttu-id="4801c-150">Dieses Modul ermöglicht es auch Kunden, Prüfungen zuzustimmen oder abzulehnen und Probleme zu melden.</span><span class="sxs-lookup"><span data-stu-id="4801c-150">This module also lets customers like or dislike reviews, and report issues.</span></span>
- <span data-ttu-id="4801c-151">**Prüfung schreiben** – Mit diesem Modul können Kunden ihre eigenen Produktprüfungen verfassen.</span><span class="sxs-lookup"><span data-stu-id="4801c-151">**Write review** – This module lets customers write their own reviews of a product.</span></span>
- <span data-ttu-id="4801c-152">**Bewertungshistogramm** – Dieses Modul enthält ein Histogramm, das den Bewertungstrend für ein Produkt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4801c-152">**Ratings histogram** – This module includes a histogram that shows the ratings trend for a product.</span></span>

<span data-ttu-id="4801c-153">Weitere Details erhalten Sie unter [Bewertungs- und Prüfungsüberblick](ratings-reviews-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4801c-153">For more details, see [Ratings and reviews overview](ratings-reviews-overview.md).</span></span>

## <a name="marketing-modules"></a><span data-ttu-id="4801c-154">Marketingmodule</span><span class="sxs-lookup"><span data-stu-id="4801c-154">Marketing modules</span></span>

<span data-ttu-id="4801c-155">Wenn Marketinginhalte für ein bestimmtes Produkt spezifisch sind, kann der PDP ein beliebiges Marketingmodul hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="4801c-155">If marketing content is unique to a specific product, any marketing module can be added to the PDP.</span></span> <span data-ttu-id="4801c-156">Sie können einer PDP Marketingmodule hinzufügen, indem Sie die Seite „anreichern“.</span><span class="sxs-lookup"><span data-stu-id="4801c-156">You can add marketing modules to a PDP by "enriching" the page.</span></span> <span data-ttu-id="4801c-157">Weitere Details finden Sie unter [Erweitern einer Produktseite](enrich-product-page.md).</span><span class="sxs-lookup"><span data-stu-id="4801c-157">For more details, see [Enrich a product page](enrich-product-page.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4801c-158">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4801c-158">Additional resources</span></span>

[<span data-ttu-id="4801c-159">Übersicht der Startseite</span><span class="sxs-lookup"><span data-stu-id="4801c-159">Home page overview</span></span>](quick-tour-home-page.md)

[<span data-ttu-id="4801c-160">Übersicht der Einkaufswagen- und Auschecken-Seiten</span><span class="sxs-lookup"><span data-stu-id="4801c-160">Cart and checkout pages overview</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="4801c-161">Übersicht der Kontenverwaltungsseiten</span><span class="sxs-lookup"><span data-stu-id="4801c-161">Account management pages overview</span></span>](quick-tour-account-management.md)

[<span data-ttu-id="4801c-162">Erweitern einer Produktdetailseite</span><span class="sxs-lookup"><span data-stu-id="4801c-162">Enrich a product details page</span></span>](enrich-product-page.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
