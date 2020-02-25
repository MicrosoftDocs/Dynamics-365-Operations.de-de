---
title: Einkaufswagenmodul
description: Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025435"
---
# <a name="cart-module"></a><span data-ttu-id="152c1-103">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="152c1-103">Cart module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="152c1-104">Dieses Thema enthält Einkaufsmodule und es wird beschrieben, wie diese den Sitesieten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="152c1-104">This topic covers cart modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="152c1-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="152c1-105">Overview</span></span>

<span data-ttu-id="152c1-106">Über ein Warenkorbmodul werden die Artikel angezeigt, die dem Warenkorb hinzugefügt wurden, bevor der Kunde zur Kasse geht.</span><span class="sxs-lookup"><span data-stu-id="152c1-106">A cart module is used to show the items that have been added to the cart before the customer proceeds to checkout.</span></span> <span data-ttu-id="152c1-107">Beispielsweise umfasst er alle Artikel, die dem Einkaufskorb und einer Auftragszusammenfassung hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="152c1-107">For example, it includes all the items that have been added to the cart and an order summary.</span></span> <span data-ttu-id="152c1-108">Außerdem kann der Kunde Werbecodes anwenden oder entfernen.</span><span class="sxs-lookup"><span data-stu-id="152c1-108">It also lets the customer apply or remove promotional codes.</span></span>

<span data-ttu-id="152c1-109">Das Einkaufskorbmodul unterstützt das Auschecken von angemeldeten Benutzern und von Gästen.</span><span class="sxs-lookup"><span data-stu-id="152c1-109">The cart module supports signed-in checkout and guest checkout.</span></span> <span data-ttu-id="152c1-110">Es unterstützt auch eine Verknüpfung **Zurück zum Einkaufen**.</span><span class="sxs-lookup"><span data-stu-id="152c1-110">It also supports a **Back to shopping** link.</span></span> <span data-ttu-id="152c1-111">Sie können die Route für diesen Link unter **Seiteneinstellungen \>Erweiterungen \>Routen** konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="152c1-111">You can configure the route for this link at **Site Settings \> Extensions \> Routes**.</span></span>

<span data-ttu-id="152c1-112">Ein Auscheckenmodul rendert Daten basierend auf der Warkenkorb-Kennung</span><span class="sxs-lookup"><span data-stu-id="152c1-112">The cart module renders data based on the cart ID.</span></span> <span data-ttu-id="152c1-113">Die Kennung ist möglicherweise ein Browsercookie, das über die Site verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="152c1-113">The cart ID is a browser cookie that is available throughout the site.</span></span>

## <a name="cart-module-properties-and-slots"></a><span data-ttu-id="152c1-114">Einkaufswagenmodul-Eigenschaften und Slots</span><span class="sxs-lookup"><span data-stu-id="152c1-114">Cart module properties and slots</span></span>

<span data-ttu-id="152c1-115">Das Wagenmodul hat eine **Überschrift**-Eigenschaft, die auf Werte wie **Einkaufstasche** und **Artikel im Einkaufskorb** gesetzt werden kann.</span><span class="sxs-lookup"><span data-stu-id="152c1-115">The cart module has a **Heading** property that can be set to values such as **Shopping bag** and **Items in your cart**.</span></span> 

## <a name="modules-that-can-be-used-in-a-cart-module"></a><span data-ttu-id="152c1-116">Module, die im Einkaufswagenmodul verwendet werden können</span><span class="sxs-lookup"><span data-stu-id="152c1-116">Modules that can be used in a cart module</span></span>

- <span data-ttu-id="152c1-117">**Textblock** – Dieses Modul unterstützt benutzerdefinierte Nachrichten im Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="152c1-117">**Text block** – This module supports custom messaging in the cart module.</span></span> <span data-ttu-id="152c1-118">Die Meldungen werden durch das Content Management-System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="152c1-118">The messages are driven by the content management system (CMS).</span></span> <span data-ttu-id="152c1-119">Es können beliebige Nachrichten hinzugefügt werden wie „Für Probleme mit der Bestellung, kontaktieren Sie 1-800-Fabrikam.“</span><span class="sxs-lookup"><span data-stu-id="152c1-119">Any message can be added, such as "For issues with your order, contact 1-800-Fabrikam."</span></span>
- <span data-ttu-id="152c1-120">**Store-Selector** – Dieses Modul wird eine Liste von nahe gelegene Filialen anzeigen, die für eine Abholung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="152c1-120">**Store selector** – This module shows a list of nearby stores where an item is available for pickup.</span></span> <span data-ttu-id="152c1-121">Hier können Benutzer einen Ort eingeben, um nach Geschäften in der Nähe zu suchen.</span><span class="sxs-lookup"><span data-stu-id="152c1-121">It lets users enter a location to find stores that are nearby.</span></span> <span data-ttu-id="152c1-122">Das Store-Selector-Modul ist in der Anwendungsprogrammierschnittstelle (API) für die Geocodierung von Bing Maps integriert, um den angegebenen Standort in eine Breite und eine Länge zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="152c1-122">The store selector module is integrated with the Bing Maps Geocoding application programming interface (API) to convert the location to a latitude and longitude.</span></span> <span data-ttu-id="152c1-123">Ein Bing Maps-API-Schlüssel ist erforderlich und muss auf der Seite „Freigegebene Retail-Parameter“ in Dynamics 365 Retail hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="152c1-123">A Bing Maps API key is required and must be added to the Retail shared parameters page in Dynamics 365 Retail.</span></span> <span data-ttu-id="152c1-124">Dieses Modul unterstützt zwei Eigenschaften: **Suchradius** und **Nutzungsbedingungen Link**.</span><span class="sxs-lookup"><span data-stu-id="152c1-124">This module supports two properties, **Search radius** and **Terms of service link**.</span></span> <span data-ttu-id="152c1-125">Die Eigenschaft **Suchradius** definiert den Suchradius für Geschäfte in Meilen.</span><span class="sxs-lookup"><span data-stu-id="152c1-125">The **Search radius** property defines the search radius for stores, in miles.</span></span> <span data-ttu-id="152c1-126">Wenn kein Wert angegeben wird, wird der Standardsuchradius von 50 Meilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="152c1-126">If no value is specified, the default search radius, 50 miles, is used.</span></span> <span data-ttu-id="152c1-127">Wenn Bings Maps oder ein externer Dienst verwendet wird, wird die Eigenschaft **Nutzungsbedingungen-Link** verwendet, um einen Link zu den Nutzungsbedingungen bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="152c1-127">If Bings Maps or any external service is used, the **Terms of service link** property can be used to provide a link to the terms of service.</span></span> <span data-ttu-id="152c1-128">Für den Bing Maps-Dienst ist ein Link zu den Nutzungsbedingungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="152c1-128">A terms of service link is required for the Bing Maps service.</span></span> 

## <a name="cart-module-settings"></a><span data-ttu-id="152c1-129">Einkaufswagen-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="152c1-129">Cart module settings</span></span>

<span data-ttu-id="152c1-130">Einkaufswagenmodule haben die folgenden Einstellungen, die unter **Site-Einstellungen \> Erweiterungen** konfiguriert werden können:</span><span class="sxs-lookup"><span data-stu-id="152c1-130">Cart modules have the following settings that can be configured at **Site Settings \> Extensions**:</span></span>

- <span data-ttu-id="152c1-131">**Höchstmenge** – Diese Eigenschaft dient zur Angabe der maximalen Anzahl jedes Artikels, die dem Einkaufskorb hinzugefügt werden kann.</span><span class="sxs-lookup"><span data-stu-id="152c1-131">**Maximum quantity** – This property is used to specify the maximum number of each item that can be added to the cart.</span></span> <span data-ttu-id="152c1-132">Beispielsweise kann ein Einzelhändler festlegen, dass nur 10 eines Produkts als einzelne Transaktion verkauft werden können.</span><span class="sxs-lookup"><span data-stu-id="152c1-132">For example, a retailer might decide that only 10 of each product can be sold in a single transaction.</span></span>
- <span data-ttu-id="152c1-133">**Bestandsscheck** – Wenn der Wert auf **Wahr** gesetzt ist, wird nur ein Artikel in den Einkaufskorb gelegt, nachdem das Kauffeldmodul sicherstellt, dass es auf Lager ist.</span><span class="sxs-lookup"><span data-stu-id="152c1-133">**Inventory check** – When the value is set to **True**, an item is added to the cart only after the buy box module makes sure that it's in stock.</span></span> <span data-ttu-id="152c1-134">Dieser ist für Bestandsscheck Szenarien ausgeführt, in denen es sich beim Artikel und für Szenarios versendet wird, wo er in Filiale aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="152c1-134">This inventory check is done both for scenarios where the item will be shipped and for scenarios where it will be picked up in the store.</span></span> <span data-ttu-id="152c1-135">Wenn der Wert auf **Falsch** gesetzt wird, wird kein Bestandsscheck geleistet, bevor ein Artikel in den Einkaufskorb gelegt wird und der Auftrag erteilt wird.</span><span class="sxs-lookup"><span data-stu-id="152c1-135">If the value is set to **False**, no inventory check is done before an item is added to the cart and the order is placed.</span></span>
- <span data-ttu-id="152c1-136">**Inventarpuffer** – Diese Eigenschaft wird verwendet, um eine Puffernummer für das Inventar anzugeben.</span><span class="sxs-lookup"><span data-stu-id="152c1-136">**Inventory buffer** – This property is used to specify a buffer number for inventory.</span></span> <span data-ttu-id="152c1-137">Bestandspuffer – Lagerbestand wird in Echtzeit verwaltet und wenn viele Debitoren Bestellungen aufgeben, kann es schwierig sein, die Lagerzählung zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="152c1-137">Inventory is maintained in real time, and when many customers place orders, it can be difficult to maintain an accurate inventory count.</span></span> <span data-ttu-id="152c1-138">Wenn ein Bestandsscheck erfolgt, und wenn der Bestand kleiner ist als der Pufferbetrag, wird das Produkt nicht als vorrätig behandelt.</span><span class="sxs-lookup"><span data-stu-id="152c1-138">When an inventory check is done, if the inventory is less than the buffer amount, the product is treated as out of stock.</span></span> <span data-ttu-id="152c1-139">Wenn Verkäufe rasch in mehreren Kanälen erfolgen und die Bestandszählung nicht vollständig synchronisiert wird, ist das Risiko kleiner, dass ein Artikel verkauft wird, der nicht vorrätig ist.</span><span class="sxs-lookup"><span data-stu-id="152c1-139">Therefore, when sales occur quickly through several channels, and the inventory count isn't fully synced, there is less risk that an item that is out of stock will be sold.</span></span>
- <span data-ttu-id="152c1-140">**Zurück zum Einkaufen** – Mit dieser Eigenschaft wird die Route für die Verknüpfung **Zurück zum Einkaufen** angegeben.</span><span class="sxs-lookup"><span data-stu-id="152c1-140">**Back to shopping** – This property is used to specify the route for the **Back to shopping** link.</span></span> <span data-ttu-id="152c1-141">Diese Route kann auf Standortebene konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="152c1-141">This route can be configured at the site level.</span></span> <span data-ttu-id="152c1-142">Mit dieser Konfiguration können Einzelhändler den Kunden zur Startseite oder einer anderen Seite auf der Website zurückführen.</span><span class="sxs-lookup"><span data-stu-id="152c1-142">This configuration lets retailers take the customer back to the home page or any other page on the site.</span></span>

## <a name="commerce-scale-unit-interaction"></a><span data-ttu-id="152c1-143">Commerce Scale Unit-Interaktion</span><span class="sxs-lookup"><span data-stu-id="152c1-143">Commerce Scale Unit interaction</span></span>

<span data-ttu-id="152c1-144">Das Einkaufskorbmoduls ruft Produktinformationen mithilfe der APIs der Commerce-Skalierungseinheit ab.</span><span class="sxs-lookup"><span data-stu-id="152c1-144">The cart module retrieves product information by using Commerce Scale Unit APIs.</span></span> <span data-ttu-id="152c1-145">Die Kennung vom Einkaufskorb vom Browsercookie wird verwendet, um die gesamte Produktinformationen der Commerce-Skalierungseinheit abzurufen.</span><span class="sxs-lookup"><span data-stu-id="152c1-145">The cart ID from the browser cookie is used to retrieve all the product information from Commerce Scale Unit.</span></span>

## <a name="add-a-cart-module-to-a-page"></a><span data-ttu-id="152c1-146">Ein Einkaufswagenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="152c1-146">Add a cart module to a page</span></span>

<span data-ttu-id="152c1-147">Um ein Einkaufswagenmodul einer neuen Seite hinzuzufügen und die erforderlichen Eigenschaften festzulegen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="152c1-147">To add a cart module to a new page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="152c1-148">Erstellen Sie ein Fragment, das mit dem Namen **Einkaufswagenfragment** bezeichnet ist und fügen Sie einen Einkaufswagenmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="152c1-148">Create a fragment that is named **Cart fragment**, and add a cart module to it.</span></span>
1. <span data-ttu-id="152c1-149">Hinzufügen eines Titels zum Einkaufswagenmodul.</span><span class="sxs-lookup"><span data-stu-id="152c1-149">Add a heading to the cart module.</span></span>
1. <span data-ttu-id="152c1-150">Fügen Sie dem Einkaufswagenmodul ein Store-Selector-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="152c1-150">Add a store selector module to the cart module.</span></span>
1. <span data-ttu-id="152c1-151">Speichern Sie das Fragment, beenden Sie die Bearbeitung und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="152c1-151">Save the fragment, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="152c1-152">Erstellen Sie eine Vorlage mit der Bezeichnung **Einkaufswagenvorlage** und fügen Sie das Einkaufswagenfragment hinzu, das Sie soeben erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="152c1-152">Create a template that is named **Cart template**, and add the cart fragment that you just created to it.</span></span>
1. <span data-ttu-id="152c1-153">Speichern Sie die Vorlage, beenden Sie die Bearbeitung und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="152c1-153">Save the template, finish editing it, and publish it.</span></span>
1. <span data-ttu-id="152c1-154">Hier können Sie eine Seite erstellen, für die die neue Vorlage verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="152c1-154">Create a page that uses the new template.</span></span>
1. <span data-ttu-id="152c1-155">Seite speichern und Vorschau anzeigen.</span><span class="sxs-lookup"><span data-stu-id="152c1-155">Save and preview the page.</span></span>
1. <span data-ttu-id="152c1-156">Beenden Sie die Bearbeitung der Seite und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="152c1-156">Finish editing the page, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="152c1-157">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="152c1-157">Additional resources</span></span>

[<span data-ttu-id="152c1-158">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="152c1-158">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="152c1-159">Containermodul</span><span class="sxs-lookup"><span data-stu-id="152c1-159">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="152c1-160">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="152c1-160">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="152c1-161">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="152c1-161">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="152c1-162">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="152c1-162">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="152c1-163">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="152c1-163">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="152c1-164">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="152c1-164">Footer module</span></span>](author-footer-module.md)
