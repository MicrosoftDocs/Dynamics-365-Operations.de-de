---
title: Kartenmodul
description: In diesem Thema werden Kartenmodule behandelt und deren Konfiguration in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
manager: annbe
ms.date: 07/31/2020
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
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: a0f5d902289c5867095e34a135c50d342f3c4f13
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646940"
---
# <a name="map-module"></a><span data-ttu-id="564a2-103">Kartenmodul</span><span class="sxs-lookup"><span data-stu-id="564a2-103">Map module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="564a2-104">In diesem Thema werden Kartenmodule behandelt und deren Konfiguration in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="564a2-104">This topic covers map modules and describes how to configure them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="564a2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="564a2-105">Overview</span></span>

<span data-ttu-id="564a2-106">Ein Kartenmodul zeigt die Standorte von Geschäften auf einer interaktiven Karte an, die mithilfe der [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/) gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="564a2-106">A map module shows the locations of stores on an interactive map that is rendered by using the [Bing Maps V8 Web Control](https://docs.microsoft.com/bingmaps/v8-web-control/).</span></span> <span data-ttu-id="564a2-107">Ein Bing Maps-API-Schlüssel ist erforderlich und muss auf der Seite „Freigegebene Parameter“ in Commerce Headquarters hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="564a2-107">A Bing Maps API key is required and must be added to the shared parameters page in Commerce headquarters.</span></span> <span data-ttu-id="564a2-108">Kartenmodule bieten verschiedene Ansichten wie Straße, Luftbild und Streetside, die Benutzer auswählen können, um Kartenpositionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="564a2-108">Map modules provide different views, such as Road, Aerial, and Streetside, that users can select to view map locations.</span></span> <span data-ttu-id="564a2-109">Sie erlauben außerdem Interaktionen wie Zoomen und die Verwendung des Standortes des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="564a2-109">They also allow for interactions such as zooming and using the user's location.</span></span>

<span data-ttu-id="564a2-110">Ein Kartenmodul ermittelt in Verbindung mit dem Shopauswahlmodul die geografischen Standorte von Geschäften, die auf einer Karte gerendert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="564a2-110">A map module works in conjunction with the store selector module to determine the geographic locations of stores that must be rendered on a map.</span></span> <span data-ttu-id="564a2-111">Die Shopauswahl- und Kartenmodule interagieren, wenn ein Benutzer ein Geschäft in einem dieser Module auf einer Seite auswählt.</span><span class="sxs-lookup"><span data-stu-id="564a2-111">Store selector and map modules interact when a user selects a store in one of those modules on a site page.</span></span> <span data-ttu-id="564a2-112">Kartenmodule können über die Interaktion mit Shopauswahlmodulen hinaus für andere Szenarien erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="564a2-112">Map modules can be extended for other scenarios, beyond interaction with store selector modules.</span></span> <span data-ttu-id="564a2-113">Eine Modulanpassung ist jedoch erforderlich.</span><span class="sxs-lookup"><span data-stu-id="564a2-113">However, module customization is required.</span></span>

<span data-ttu-id="564a2-114">Das Kartenmodul wurde in der Commerce-Version 10.0.13 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="564a2-114">The map module was introduced in Commerce version 10.0.13.</span></span>

<span data-ttu-id="564a2-115">Das folgende Bild zeigt ein Beispiel eines Kartenmoduls, das auf einer Ladenstandortseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="564a2-115">The following image shows an example of a map module that is used on a store locations page.</span></span>

![Beispiel eines Shopauswahlmoduls](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a><span data-ttu-id="564a2-117">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="564a2-117">Module properties</span></span>

| <span data-ttu-id="564a2-118">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="564a2-118">Property name</span></span>             | <span data-ttu-id="564a2-119">Wert</span><span class="sxs-lookup"><span data-stu-id="564a2-119">Value</span></span>                 | <span data-ttu-id="564a2-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="564a2-120">Description</span></span> |
|---------------------------|-----------------------|-------------|
| <span data-ttu-id="564a2-121">Überschrift</span><span class="sxs-lookup"><span data-stu-id="564a2-121">Heading</span></span> | <span data-ttu-id="564a2-122">Text</span><span class="sxs-lookup"><span data-stu-id="564a2-122">Text</span></span> | <span data-ttu-id="564a2-123">Die Überschrift für das Modul.</span><span class="sxs-lookup"><span data-stu-id="564a2-123">The heading for the module.</span></span> |
| <span data-ttu-id="564a2-124">Reißzweckenoptionen: Standardsymbol</span><span class="sxs-lookup"><span data-stu-id="564a2-124">Pushpin options: Default icon</span></span> | <span data-ttu-id="564a2-125">Bild</span><span class="sxs-lookup"><span data-stu-id="564a2-125">Image</span></span> | <span data-ttu-id="564a2-126">Das Reißzweckensymbol, das für Geschäfte verwendet werden soll, die auf einer Karte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="564a2-126">The pushpin symbol image to use for stores that are shown on a map.</span></span> |
| <span data-ttu-id="564a2-127">Reißzweckenoptionen: Aktives Symbol</span><span class="sxs-lookup"><span data-stu-id="564a2-127">Pushpin options: Active icon</span></span> | <span data-ttu-id="564a2-128">Bild</span><span class="sxs-lookup"><span data-stu-id="564a2-128">Image</span></span> | <span data-ttu-id="564a2-129">Das Reißzweckensymbol, das für ein Geschäft verwendet werden soll, das auf einer Karte ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="564a2-129">The pushpin symbol image to use for a store that is selected on a map.</span></span> |
| <span data-ttu-id="564a2-130">Reißzweckenoptionen: Standardsymbolfarbe</span><span class="sxs-lookup"><span data-stu-id="564a2-130">Pushpin options: Default icon color</span></span> | <span data-ttu-id="564a2-131">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="564a2-131">Character string</span></span> | <span data-ttu-id="564a2-132">Der Text- oder Hexadezimalwert für die Farbe der Reißzweckensymbole auf einer Karte.</span><span class="sxs-lookup"><span data-stu-id="564a2-132">The text or hexadecimal value for the color of pushpin symbols on a map.</span></span> |
| <span data-ttu-id="564a2-133">Reißzweckenoptionen: Farbe aktives Symbol</span><span class="sxs-lookup"><span data-stu-id="564a2-133">Pushpin options: Active icon color</span></span> | <span data-ttu-id="564a2-134">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="564a2-134">Character string</span></span> | <span data-ttu-id="564a2-135">Der Text- oder Hexadezimalwert für die Farbe der auf einer Karte ausgewählten Reißzweckensymbole.</span><span class="sxs-lookup"><span data-stu-id="564a2-135">The text or hexadecimal value for the color of selected pushpin symbols on a map.</span></span> |
| <span data-ttu-id="564a2-136">Index anzeigen</span><span class="sxs-lookup"><span data-stu-id="564a2-136">Show index</span></span> | <span data-ttu-id="564a2-137">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="564a2-137">**True** or **False**</span></span> | <span data-ttu-id="564a2-138">Wenn diese Eigenschaft auf **Wahr** gesetzt wird, zeigt jedes Reißzweckensymbol, das für ein Geschäft steht, eine Zahl an.</span><span class="sxs-lookup"><span data-stu-id="564a2-138">If this property is set to **True**, every pushpin symbol that indicates a store will show an index.</span></span> <span data-ttu-id="564a2-139">Diese Zahl stimmt mit der Zahl in der Listenansicht überein, die das Shopauswahlmodul anzeigt.</span><span class="sxs-lookup"><span data-stu-id="564a2-139">This index will match the index in the list view that the store selector module shows.</span></span> |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a><span data-ttu-id="564a2-140">Zulässige Kartierungs-URLs zu den Inhaltssicherheitsrichtlinien einer Website hinzufügen</span><span class="sxs-lookup"><span data-stu-id="564a2-140">Add allowed mapping URLs to a site's content security policy directives</span></span>

<span data-ttu-id="564a2-141">Damit das Kartenmodul mit Bing Karten interagieren kann, müssen Sie sicherstellen, dass die folgenden Kartierungs-URLs gemäß der Inhaltssicherheitsrichtlinie Ihrer Website zulässig sind (also auf der „Whitelist“ stehen).</span><span class="sxs-lookup"><span data-stu-id="564a2-141">For the maps module to interact with Bing Maps, you must ensure that the following mapping URLs are allowed (also known as "whitelisted") per your site's content security policy (CSP).</span></span> <span data-ttu-id="564a2-142">Diese Einstellung erfolgt im Commerce Site Builder, indem zulässige URLs zu verschiedenen Inhaltssicherheitsrichtlinie der Website hinzugefügt werden (z. B. **img-src**).</span><span class="sxs-lookup"><span data-stu-id="564a2-142">This setup is done in Commerce site builder, by adding allowed URLs to various site CSP directives (for example, **img-src**).</span></span> <span data-ttu-id="564a2-143">Weitere Informationen finden Sie unter [Inhaltssicherheitsrichtlinie](manage-csp.md).</span><span class="sxs-lookup"><span data-stu-id="564a2-143">For more information, see [Content security policy](manage-csp.md).</span></span> 

- <span data-ttu-id="564a2-144">Fügen Sie der **connect-src**-Richtlinie **&#42;.bing.com** hinzu.</span><span class="sxs-lookup"><span data-stu-id="564a2-144">To the **connect-src** directive, add **&#42;.bing.com**.</span></span>
- <span data-ttu-id="564a2-145">Fügen Sie der **img-src**-Richtlinie **&#42;.virtualearth.net** hinzu.</span><span class="sxs-lookup"><span data-stu-id="564a2-145">To the **img-src** directive, add **&#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="564a2-146">Fügen Sie zur **script-src**-Richtlinie **&#42;.bing.com, &#42;.virtualearth.net** hinzu.</span><span class="sxs-lookup"><span data-stu-id="564a2-146">To the **script-src** directive, add **&#42;.bing.com, &#42;.virtualearth.net**.</span></span>
- <span data-ttu-id="564a2-147">Fügen Sie der **script style-src**-Richtlinie **&#42;.bing.com** hinzu.</span><span class="sxs-lookup"><span data-stu-id="564a2-147">To the **script style-src** directive, add **&#42;.bing.com**.</span></span>

## <a name="add-a-map-module-to-a-page"></a><span data-ttu-id="564a2-148">Ein Kartenmodul einer Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="564a2-148">Add a map module to a page</span></span>

<span data-ttu-id="564a2-149">Ausführliche Informationen zum Konfigurieren eines Kartenmoduls auf einer Seite finden Sie unter [Shopauswahlmodul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="564a2-149">For detailed information about how to configure a map module on a page, see [Store selector module](store-selector.md).</span></span> 
 
## <a name="additional-resources"></a><span data-ttu-id="564a2-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="564a2-150">Additional resources</span></span>

[<span data-ttu-id="564a2-151">Überblick über das Starterkit</span><span class="sxs-lookup"><span data-stu-id="564a2-151">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="564a2-152">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="564a2-152">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="564a2-153">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="564a2-153">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="564a2-154">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="564a2-154">Store selector module</span></span>](store-selector.md)

[<span data-ttu-id="564a2-155">Bing Maps für Ihr Unternehmen verwalten</span><span class="sxs-lookup"><span data-stu-id="564a2-155">Manage Bing Maps for your organization</span></span>](./dev-itpro/manage-bing-maps.md)

[<span data-ttu-id="564a2-156">Bing Maps V8 Web Control</span><span class="sxs-lookup"><span data-stu-id="564a2-156">Bing Maps V8 Web Control</span></span>](https://docs.microsoft.com/bingmaps/v8-web-control/)
