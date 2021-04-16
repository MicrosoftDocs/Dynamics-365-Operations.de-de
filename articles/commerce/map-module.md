---
title: Kartenmodul
description: Dieses Thema behandelt Kartenmodule und beschreibt deren Konfiguration in Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: b8c3ab0653fd5e3561d0bfbe85624d912756e2be
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794186"
---
# <a name="map-module"></a><span data-ttu-id="b854c-103">Kartenmodul</span><span class="sxs-lookup"><span data-stu-id="b854c-103">Map module</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="b854c-104">Dieses Thema behandelt Kartenmodule und beschreibt deren Konfiguration in Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b854c-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b854c-105">Ein Kartenmodul zeigt die Standorte von Geschäften auf einer interaktiven Karte an, die mithilfe der [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/) gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="b854c-105">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="b854c-106">Ein Bing Maps-API-Schlüssel ist erforderlich und muss auf der Seite „Freigegebene Parameter“ in Commerce Headquarters hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b854c-106">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="b854c-107">Kartenmodule bieten verschiedene Ansichten wie Straße, Luftbild und Streetside, die Benutzer auswählen können, um Kartenpositionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b854c-107">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="b854c-108">Sie erlauben außerdem Interaktionen wie Zoomen und die Verwendung des Standortes des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b854c-108">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="b854c-109">Ein Kartenmodul ermittelt in Verbindung mit dem Shopauswahlmodul die geografischen Standorte von Geschäften, die auf einer Karte gerendert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b854c-109">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="b854c-110">Die Shopauswahl- und Kartenmodule interagieren, wenn ein Benutzer ein Geschäft in einem dieser Module auf einer Seite auswählt.</span><span class="sxs-lookup"><span data-stu-id="b854c-110">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="b854c-111">Kartenmodule können über die Interaktion mit Shopauswahlmodulen hinaus für andere Szenarien erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="b854c-111">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="b854c-112">Eine Modulanpassung ist jedoch erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b854c-112">However, module customization is required.</span></span>

> [!NOTE]
> <span data-ttu-id="b854c-113">Das Kartenmodul ist in der Dynamics 365 Commerce-Version 10.0.13 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b854c-113">The map module is available in the Dynamics 365 Commerce 10.0.13 release.</span></span>

<span data-ttu-id="b854c-114">Das folgende Bild zeigt ein Beispiel eines Kartenmoduls, das auf einer Ladenstandortseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b854c-114">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Beispiel eines Shopauswahlmoduls](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="b854c-116">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="b854c-116">Module properties</span></span>

| <span data-ttu-id="b854c-117">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="b854c-117">Property name</span></span>             | <span data-ttu-id="b854c-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b854c-118">Value</span></span>                 | <span data-ttu-id="b854c-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b854c-119">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="b854c-120">Überschrift</span><span class="sxs-lookup"><span data-stu-id="b854c-120">Heading</span></span> | <span data-ttu-id="b854c-121">Text</span><span class="sxs-lookup"><span data-stu-id="b854c-121">Text</span></span> | <span data-ttu-id="b854c-122">Die Überschrift für das Modul.</span><span class="sxs-lookup"><span data-stu-id="b854c-122">The heading for the module.</span></span> |
| <span data-ttu-id="b854c-123">Reißzweckenoptionen: Standardsymbol</span><span class="sxs-lookup"><span data-stu-id="b854c-123">Pushpin options: Default icon</span></span> | <span data-ttu-id="b854c-124">Bild</span><span class="sxs-lookup"><span data-stu-id="b854c-124">Image</span></span> | <span data-ttu-id="b854c-125">Das Reißzweckensymbol, das für Geschäfte verwendet werden soll, die auf einer Karte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="b854c-125">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="b854c-126">Reißzweckenoptionen: Aktives Symbol</span><span class="sxs-lookup"><span data-stu-id="b854c-126">Pushpin options: Active icon</span></span> | <span data-ttu-id="b854c-127">Bild</span><span class="sxs-lookup"><span data-stu-id="b854c-127">Image</span></span> | <span data-ttu-id="b854c-128">Das Reißzweckensymbol, das für ein Geschäft verwendet werden soll, das auf einer Karte ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b854c-128">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="b854c-129">Reißzweckenoptionen: Standardsymbolfarbe</span><span class="sxs-lookup"><span data-stu-id="b854c-129">Pushpin options: Default icon color</span></span> | <span data-ttu-id="b854c-130">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b854c-130">Character string</span></span> | <span data-ttu-id="b854c-131">Der Text- oder Hexadezimalwert für die Farbe der Reißzweckensymbole auf einer Karte.</span><span class="sxs-lookup"><span data-stu-id="b854c-131">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="b854c-132">Reißzweckenoptionen: Farbe aktives Symbol</span><span class="sxs-lookup"><span data-stu-id="b854c-132">Pushpin options: Active icon color</span></span> | <span data-ttu-id="b854c-133">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="b854c-133">Character string</span></span> | <span data-ttu-id="b854c-134">Der Text- oder Hexadezimalwert für die Farbe der auf einer Karte ausgewählten Reißzweckensymbole.</span><span class="sxs-lookup"><span data-stu-id="b854c-134">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="b854c-135">Index anzeigen</span><span class="sxs-lookup"><span data-stu-id="b854c-135">Show index</span></span> | <span data-ttu-id="b854c-136">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="b854c-136">**True** or **False**</span></span> | <span data-ttu-id="b854c-137">Wenn diese Eigenschaft auf **Wahr** gesetzt wird, zeigt jedes Reißzweckensymbol, das für ein Geschäft steht, eine Zahl an.</span><span class="sxs-lookup"><span data-stu-id="b854c-137">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="b854c-138">Diese Zahl stimmt mit der Zahl in der Listenansicht überein, die das Shopauswahlmodul anzeigt.</span><span class="sxs-lookup"><span data-stu-id="b854c-138">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="b854c-139">Zulässige Kartierungs-URLs zu den Inhaltssicherheitsrichtlinien einer Website hinzufügen</span><span class="sxs-lookup"><span data-stu-id="b854c-139">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="b854c-140">Damit das Kartenmodul mit Bing Karten interagieren kann, müssen Sie sicherstellen, dass die folgenden Zuordnungs-URLs gemäß der Inhaltssicherheitsrichtlinie (CSP) Ihrer Website zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="b854c-140">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed per your site's content security policy (CSP).</span></span> <span data-ttu-id="b854c-141">Diese Einstellung erfolgt im Commerce Site Builder, indem zulässige URLs zu verschiedenen Inhaltssicherheitsrichtlinie der Website hinzugefügt werden (z. B. **img-src**).</span><span class="sxs-lookup"><span data-stu-id="b854c-141">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="b854c-142">Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="b854c-142">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="b854c-143">Fügen Sie der **connect-src**-Richtlinie **&#42;.bing.com** hinzu.</span><span class="sxs-lookup"><span data-stu-id="b854c-143">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="b854c-144">Fügen Sie der **img-src**-Richtlinie **&#42;.virtualearth.net** hinzu.</span><span class="sxs-lookup"><span data-stu-id="b854c-144">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="b854c-145">Fügen Sie zur **script-src**-Richtlinie **&#42;.bing.com, &#42;.virtualearth.net** hinzu.</span><span class="sxs-lookup"><span data-stu-id="b854c-145">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="b854c-146">Fügen Sie der **script style-src**-Richtlinie **&#42;.bing.com** hinzu.</span><span class="sxs-lookup"><span data-stu-id="b854c-146">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="b854c-147">Ein Kartenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="b854c-147">Add a map module to a page</span></span>

<span data-ttu-id="b854c-148">Ausführliche Informationen zum Konfigurieren eines Kartenmoduls auf einer Seite finden Sie unter [Shopauswahlmodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="b854c-148">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="b854c-149">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b854c-149">Additional resources</span></span>

[<span data-ttu-id="b854c-150">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="b854c-150">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b854c-151">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="b854c-151">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="b854c-152">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="b854c-152">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="b854c-153">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="b854c-153">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="b854c-154">Bing Karten für Ihr Unternehmen verwalten</span><span class="sxs-lookup"><span data-stu-id="b854c-154">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="b854c-155">Bing Maps V8 Web Control</span><span class="sxs-lookup"><span data-stu-id="b854c-155">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]