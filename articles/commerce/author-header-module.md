---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 04/13/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cec138ebefbd2beb2f1cf6302ce58d8bbc5c4bbd
ms.sourcegitcommit: ac966ea3a6c557fb5f9634b187b0e788d3e82d4d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2020
ms.locfileid: "3261443"
---
# <a name="header-module"></a><span data-ttu-id="4f9fb-103">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-103">Header module</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4f9fb-104">In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="4f9fb-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="4f9fb-105">Overview</span></span>

<span data-ttu-id="4f9fb-106">Im Dynamics 365 Commerce umfasst ein Seitenkopf mehrere Module, z. B. die Module Kopfzeile, Navigationsmenü, Suche, Werbebanner und Cookie-Einwilligung.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="4f9fb-107">Das Kopfzeilenmodul enthält ein Site-Logo, Links zur Navigationshierarchie, Links zu anderen Seiten der Site, ein Warenkorbsymbol, ein Wunschliste-Symbol, Anmeldeoptionen und die Suchleiste.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="4f9fb-108">Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site angezeigt wird (anders ausgedrückt für ein Desktopgerät oder ein mobiles Gerät).</span><span class="sxs-lookup"><span data-stu-id="4f9fb-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="4f9fb-109">Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="4f9fb-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header-module"></a><span data-ttu-id="4f9fb-110">Eigenschaften eines Kopfmoduls</span><span class="sxs-lookup"><span data-stu-id="4f9fb-110">Properties of a header module</span></span>

<span data-ttu-id="4f9fb-111">Ein Kopfmodul unterstützt die Eigenschaften **Logo-Bild**, **Logo-Link** und **Meine Kontolinks**.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-111">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="4f9fb-112">Die Eigenschaften **Logo-Bild** und **Logo-Link** werden verwendet, um ein Logo auf der Seite zu definieren.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-112">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="4f9fb-113">Weitere Informationen finden Sie in [Hinzufügen eines Logos](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="4f9fb-113">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="4f9fb-114">Die Eigenschaft **Meine Kontolinks** kann verwendet werden, um Kontoseiten zu bestimmen, für die der Websitebesitzer Quicklinks in der Kopfzeile anzeigen möchte.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-114">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="4f9fb-115">Module, die in einem Kopfzeilenmodul verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="4f9fb-115">Modules that are available in a header module</span></span>

<span data-ttu-id="4f9fb-116">Die folgenden Module können im Kopfzeilenmodul verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="4f9fb-116">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="4f9fb-117">**Navigationsmenü** – Das Navigationsmenü stellt die Kanalnavigationshierarchie und anderen statischen Navigationslinks dar.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-117">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="4f9fb-118">Die Kanalnavigationshierarchie kann in Dynamics 365 Commerce konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-118">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="4f9fb-119">Das Navigationsmenü hat eine Eigenschaft **Navigationsquelle**, mit der die Retail Server-Navigationsmenüelemente und statische Menüelemente als Quelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-119">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="4f9fb-120">Wenn statische Menüelemente als Quelle angegeben werden, können relative Links zu anderen Seiten auf der Site bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-120">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="4f9fb-121">Konfigurierte Artikel werden dann als Kopfzeilennavigation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-121">Configured items then appear as header navigation.</span></span> 
- <span data-ttu-id="4f9fb-122">**Suche** – Das Suchmodul ermöglicht es Benutzern, Suchbegriffe einzugeben, sodass sie nach Produkten suchen können.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-122">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="4f9fb-123">Die URL der Standardsuchseite und die Suchabfrageparameter müssen unter **Seiteneinstellungen \> Erweiterungen** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-123">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="4f9fb-124">Das Suchmodul verfügt über Eigenschaften, mit denen Sie die Suchschaltfläche oder -Bezeichnung nach Bedarf unterdrücken können.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-124">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="4f9fb-125">Das Suchmodul unterstützt auch automatische Vorschlagsoptionen wie Produkt-, Keyword- und Kategoriesuchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-125">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>
- <span data-ttu-id="4f9fb-126">**Warenkorbsymbol** – Das Warenkorbsymbolmodul stellt das Warenkorbsymbol dar, das die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-126">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="4f9fb-127">Weitere Informationen finden Sie unter [Warenkorb-Symbolmodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="4f9fb-127">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="4f9fb-128">Erstellen eines Kopfzeilenmoduls für eine Seite</span><span class="sxs-lookup"><span data-stu-id="4f9fb-128">Create a header module for a page</span></span>

<span data-ttu-id="4f9fb-129">Um ein neues Kopfzeilenmodul zu erstellen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-129">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="4f9fb-130">Erstellen Sie ein Fragment, das **Kopfzeilenfragment** heißt, und fügen Sie ein Containermodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-130">Create a fragment that is named **Header fragment**, and add a container module to it.</span></span>
1. <span data-ttu-id="4f9fb-131">Legen Sie im Eigenschaftsfenster für das Containermodul die Eigenschaft **Breite** auf **Container füllen** fest.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-131">In the property pane for the container module, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="4f9fb-132">Fügen Sie dem Containermodul ein Werbebanner- und Cookie-Zustimmungsmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-132">Add a promo banner and cookie consent modules to the container module.</span></span>
1. <span data-ttu-id="4f9fb-133">Fügen Sie dem Fragment ein weiteres Containermodul hinzu und legen Sie die Eigenschaft **Breite** auf **Container füllen** fest.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-133">Add another container module to the fragment, and set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="4f9fb-134">Fügen Sie dem zweiten Containermodul ein Kopfzeilenmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-134">Add a header module to the second container module.</span></span>
1. <span data-ttu-id="4f9fb-135">Fügen Sie im Slot **Navigationsmenü** des Kopfzeilenmoduls ein Navigationsmenümodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-135">In the **Navigation menu** slot of the header module, add a navigation menu module.</span></span> 
1. <span data-ttu-id="4f9fb-136">Konfigurieren Sie im Eigenschaftenbereich für das Navigationsmenümodul die Eigenschaften des Navigationsmenümoduls.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-136">In the property pane for the navigation menu module, configure the properties of the navigation menu module.</span></span>
1. <span data-ttu-id="4f9fb-137">Fügen Sie im Slot **Suche** des Kopfzeilenmoduls ein Suchmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-137">In the **Search** slot of the header module, add a search module.</span></span> 
1. <span data-ttu-id="4f9fb-138">Konfigurieren Sie im Eigenschaftenbereich für das Suchmodul die Eigenschaften des Suchmoduls.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-138">In the property pane for the search module, configure the properties of the search module.</span></span> 
1. <span data-ttu-id="4f9fb-139">In dem Slot **Warenkorbsymbol** fügen Sie im Steckplatz des Header-Moduls ein Warenkorbsymbol-Modul hinzu.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-139">In the **Cart icon** slot of the header module, add a cart icon module.</span></span> 
1. <span data-ttu-id="4f9fb-140">Konfigurieren Sie im Eigenschaftenbereich für das Warenkorbmodul die Eigenschaften des Warenkorbmoduls.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-140">In the property pane for the cart icon module, configure the properties of the cart icon module.</span></span> <span data-ttu-id="4f9fb-141">Wenn das Warenkorbsymbol beim Bewegen des Mauszeigers einen Mini-Warenkorb anzeigen soll, wählen Sie **Wahr**, um **Mini-Warenkorb anzuzeigen**.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-141">If you want the cart icon to display a mini cart when hovered over, select **True** for **Show mini cart**.</span></span>
1. <span data-ttu-id="4f9fb-142">Speichern Sie das Seitenfragment, beenden Sie die Bearbeitung und veröffentlichen Sie diese.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-142">Save the page fragment, finish editing, and publish it.</span></span> 


<span data-ttu-id="4f9fb-143">Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-143">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="4f9fb-144">Fügen Sie im Slot **Haupt** auf der Standardseite das Kopfzeilenseitenfragment hinzu, das das Kopfzeilenmodul der Kopfzeile enthält.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-144">In the **Main** slot of the default page, add the header page fragment that contains the header module to the header.</span></span>
1. <span data-ttu-id="4f9fb-145">Speichern Sie die Vorlage, beenden Sie die Bearbeitung und veröffentlichen Sie diese.</span><span class="sxs-lookup"><span data-stu-id="4f9fb-145">Save the template, finish editing, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f9fb-146">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4f9fb-146">Additional resources</span></span>

[<span data-ttu-id="4f9fb-147">Starterkit-Übersicht</span><span class="sxs-lookup"><span data-stu-id="4f9fb-147">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="4f9fb-148">Containermodul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-148">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="4f9fb-149">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-149">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="4f9fb-150">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-150">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="4f9fb-151">Symbol Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-151">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="4f9fb-152">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-152">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="4f9fb-153">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-153">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="4f9fb-154">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-154">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="4f9fb-155">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="4f9fb-155">Footer module</span></span>](author-footer-module.md)
