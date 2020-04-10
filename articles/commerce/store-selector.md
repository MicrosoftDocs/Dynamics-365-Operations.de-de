---
title: Shopauswahlmodul
description: Dieses Thema enthält das Shopauswahlmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8efc2345ded52bfaee2d400815795906f326f4fd
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/21/2020
ms.locfileid: "3157339"
---
# <a name="store-selector-module"></a><span data-ttu-id="5cdd3-103">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="5cdd3-103">Store selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5cdd3-104">Dieses Thema enthält das Shopauswahlmodul und es wird beschrieben, wie es Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-104">This topic covers the store selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="5cdd3-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="5cdd3-105">Overview</span></span>

<span data-ttu-id="5cdd3-106">Ein Shopauswahlmodul wird für das Kundenszenario „Online kaufen, im Geschäft abholen“ (BOPIS) verwendet.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-106">A store selector module is used for the "buy online, pick up in store"" (BOPIS) customer scenario.</span></span> <span data-ttu-id="5cdd3-107">Es zeigt eine Liste der Geschäfte an, in denen ein Produkt zur Abholung verfügbar ist, sowie die Öffnungszeiten und den Produktbestand für jedes Geschäft.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-107">It displays a list of stores where a product is available for pickup, as well as store hours and product inventory for each store.</span></span>

<span data-ttu-id="5cdd3-108">Das Shopauswahlmodul benötigt den Kontext eines Produkts und einen Suchort, um Filialen zu finden.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-108">The store selector module requires the context of a product and a search location to find stores.</span></span> <span data-ttu-id="5cdd3-109">Wenn kein Suchort vorhanden ist, wird standardmäßig der Browserstandort des Kunden verwendet, sofern der Kunde seine Zustimmung erteilt.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-109">In the absence of a search location, it defaults to the customer's browser location, provided that the customer gives consent.</span></span> <span data-ttu-id="5cdd3-110">Das Modul verfügt über ein Eingabefeld, in das der Kunde einen Ort (Postleitzahl oder Stadt und Bundesland) eingeben kann, um Geschäfte in der Nähe zu finden.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-110">The module has an input box which allows the customer to enter a location (zipcode, or city and state) to find stores that are nearby.</span></span>

<span data-ttu-id="5cdd3-111">Das Store-Selector-Modul ist in der Anwendungsprogrammierschnittstelle (API) für die Geocodierung von Bing Maps integriert, um den angegebenen Standort in eine Breite und eine Länge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-111">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="5cdd3-112">Ein Bing Maps-API-Schlüssel ist erforderlich und muss auf der Seite „Freigegebene Commerce-Parameter“ in Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-112">A Bing Maps API key is required and must be added to the Commerce shared parameters page in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5cdd3-113">Das Shopauswahlmodul kann einem Kaufboxmodul auf der Produktdetailseite (PDP) hinzugefügt werden, um Filialen anzuzeigen, in denen ein Produkt zur Abholung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-113">The store selector module can be added to a buy box module on the product details page (PDP) to display stores where a product is available for pickup.</span></span> <span data-ttu-id="5cdd3-114">Es kann auch einem Einkaufswagenmodul hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-114">It can also be added to a cart module.</span></span> <span data-ttu-id="5cdd3-115">Beim Hinzufügen zu einem Einkaufswagenmodul zeigt das Shopauswahlmodul Abholoptionen für jede Einkaufswagenposition an.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-115">When added to a cart module, the store selector module displays pickup options for each cart line item.</span></span> <span data-ttu-id="5cdd3-116">Darüber hinaus kann dieses Modul mit benutzerdefinierter Codierung über Erweiterungen und Anpassungen zu anderen Seiten oder Modulen hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-116">In addition, with custom coding this module can be added to other pages or modules via extensions and customizations.</span></span>

<span data-ttu-id="5cdd3-117">Damit das BOPIS-Szenario funktioniert, sollten Produkte mit dem Liefermodus „Kundenabholung“ konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-117">For the BOPIS scenario to work, products should be configured with the "customer pickup" delivery mode.</span></span> <span data-ttu-id="5cdd3-118">Andernfalls wird das Modul nicht auf den jeweiligen Seiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-118">Otherwise, the module will not be shown on the respective pages.</span></span> <span data-ttu-id="5cdd3-119">Einzelheiten zum Konfigurieren des Übermittlungsmodus finden Sie unter [Lieferarten einrichten](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span><span class="sxs-lookup"><span data-stu-id="5cdd3-119">For details on how to configure the delivery mode, see [Set up modes of delivery](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery).</span></span>

<span data-ttu-id="5cdd3-120">Das folgende Bild zeigt ein Beispiel eines Speicherauswahlmoduls, das auf einem PDP verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-120">The following image shows an example of a store selector module used on a PDP.</span></span>

![Beispiel eines Shopauswahlmoduls](./media/BOPIS.PNG)

## <a name="store-selector-module-usage-in-e-commerce"></a><span data-ttu-id="5cdd3-122">Speichern Sie die Verwendung des Auswahlmoduls im E-Commerce</span><span class="sxs-lookup"><span data-stu-id="5cdd3-122">Store selector module usage in e-Commerce</span></span>

- <span data-ttu-id="5cdd3-123">Ein Shopauswahlmodul kann auf einer Produktdetailseite (PDP) verwendet werden, um Filialen in der Nähe zu finden, in denen ein Produkt zur Abholung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-123">A store selector module can be used on a product details page (PDP) to find nearby stores where a product is available for pickup.</span></span>
- <span data-ttu-id="5cdd3-124">Ein Shopauswahlmodul kann auf einer Einkaufswagenseite verwendet werden, um Filialen in der Nähe zu finden, in denen ein Produkt im Einkaufswagen zur Abholung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-124">A store selector module can be used on a cart page to find nearby stores where a product in the cart is available for pickup.</span></span>

## <a name="store-selector-module-properties"></a><span data-ttu-id="5cdd3-125">Eigenschaften des Shopauswahlmoduls</span><span class="sxs-lookup"><span data-stu-id="5cdd3-125">Store selector module properties</span></span>

| <span data-ttu-id="5cdd3-126">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="5cdd3-126">Property name</span></span>             | <span data-ttu-id="5cdd3-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5cdd3-127">Value</span></span>                 | <span data-ttu-id="5cdd3-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cdd3-128">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="5cdd3-129">Suchradius</span><span class="sxs-lookup"><span data-stu-id="5cdd3-129">Search radius</span></span> | <span data-ttu-id="5cdd3-130">Nummer</span><span class="sxs-lookup"><span data-stu-id="5cdd3-130">Number</span></span> | <span data-ttu-id="5cdd3-131">Definiert den Suchradius für Geschäfte in Meilen.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-131">Defines the search radius for stores, in miles.</span></span> <span data-ttu-id="5cdd3-132">Wenn kein Wert angegeben wird, wird der Standardsuchradius von 50 Meilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-132">If no value is specified, the default search radius of 50 miles is used.</span></span>|
|<span data-ttu-id="5cdd3-133">Allgemeine Geschäftsbedingungen</span><span class="sxs-lookup"><span data-stu-id="5cdd3-133">Terms of Service</span></span> | <span data-ttu-id="5cdd3-134">URL</span><span class="sxs-lookup"><span data-stu-id="5cdd3-134">URL</span></span>    |  <span data-ttu-id="5cdd3-135">Für den Bing Maps-Dienst ist die URL zu den Nutzungsbedingungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-135">The terms of service URL that is required for the Bing Maps service.</span></span> |

## <a name="add-a-store-selector-module-to-a-page"></a><span data-ttu-id="5cdd3-136">Hinzufügen eines Shopauswahlmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="5cdd3-136">Add a store selector module to a page</span></span>

<span data-ttu-id="5cdd3-137">Ein Shopauswahlmodul benötigt den Kontext eines Produkts und kann daher nur in Kauffeld- und Einkaufswagenmodulen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-137">A store selector module needs the context of a product, so it can only be used within buy box and cart modules.</span></span> <span data-ttu-id="5cdd3-138">Shopauswahlmodule funktionieren außerhalb dieser Module nicht.</span><span class="sxs-lookup"><span data-stu-id="5cdd3-138">Store selector modules do not function outside these modules.</span></span>

- <span data-ttu-id="5cdd3-139">Informationen zum Hinzufügen eines Shopauswahlmoduls zu einem Kauffeldmodul finden Sie unter [Kauffeldmodul](add-buy-box.md).</span><span class="sxs-lookup"><span data-stu-id="5cdd3-139">For information on how to add a store selector module to a buy box module, see [Buy box module](add-buy-box.md).</span></span> 
- <span data-ttu-id="5cdd3-140">Informationen zum Hinzufügen eines Shopauswahlmoduls zu einem Einkaufswagenmodul finden Sie unter [Einkaufswagenmodul](add-cart-module.md)</span><span class="sxs-lookup"><span data-stu-id="5cdd3-140">For information on how to add a store selector module to a cart module, see [Cart module](add-cart-module.md)</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5cdd3-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5cdd3-141">Additional resources</span></span>

[<span data-ttu-id="5cdd3-142">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="5cdd3-142">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5cdd3-143">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="5cdd3-143">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5cdd3-144">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="5cdd3-144">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="5cdd3-145">Schnelleinführung zur Produktdetailseite</span><span class="sxs-lookup"><span data-stu-id="5cdd3-145">Quick tour of PDP</span></span>](quick-tour-pdp.md)

[<span data-ttu-id="5cdd3-146">Schnelleinführung zum Einkaufskorb und Auscheckvorgang</span><span class="sxs-lookup"><span data-stu-id="5cdd3-146">Quick tour of Cart and checkout</span></span>](quick-tour-cart-checkout.md)

[<span data-ttu-id="5cdd3-147">Lieferarten einrichten</span><span class="sxs-lookup"><span data-stu-id="5cdd3-147">Set up modes of delivery</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-modes-of-delivery)
