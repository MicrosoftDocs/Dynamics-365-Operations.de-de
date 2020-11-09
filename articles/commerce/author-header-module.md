---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 52069af5ca2211473d4a096ad850b5be1290bba1
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055449"
---
# <a name="header-module"></a><span data-ttu-id="9a111-103">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="9a111-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9a111-104">In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9a111-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="9a111-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="9a111-105">Overview</span></span>

<span data-ttu-id="9a111-106">In Dynamics 365 Commerce wird eine Seitenkopfzeile als Seitenfragment konfiguriert, das die Module Kopfzeile, Werbebanner und Cookie-Zustimmung enthält.</span><span class="sxs-lookup"><span data-stu-id="9a111-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="9a111-107">Das Kopfzeilenmodul enthält ein Site-Logo, Links zur Navigationshierarchie, Links zu anderen Seiten der Site, ein Warenkorbsymbolmodul, ein Wunschliste-Symbol, Anmeldeoptionen und die Suchleiste.</span><span class="sxs-lookup"><span data-stu-id="9a111-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="9a111-108">Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site angezeigt wird (anders ausgedrückt für ein Desktopgerät oder ein mobiles Gerät).</span><span class="sxs-lookup"><span data-stu-id="9a111-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="9a111-109">Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="9a111-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu* ).</span></span>

<span data-ttu-id="9a111-110">Das folgende Bild zeigt ein Beispiel eines Kopfzeilenmoduls, das auf einer Startseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9a111-110">The following image shows an example of a header module on a home page.</span></span>

![Beispiel eines Kopfzeilenmoduls](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="9a111-112">Eigenschaften eines Kopfmoduls</span><span class="sxs-lookup"><span data-stu-id="9a111-112">Properties of a header module</span></span>

<span data-ttu-id="9a111-113">Ein Kopfmodul unterstützt die Eigenschaften **Logo-Bild** , **Logo-Link** und **Meine Kontolinks**.</span><span class="sxs-lookup"><span data-stu-id="9a111-113">A header module supports **Logo image** , **Logo link** , and **My account links** properties.</span></span> 

<span data-ttu-id="9a111-114">Die Eigenschaften **Logo-Bild** und **Logo-Link** werden verwendet, um ein Logo auf der Seite zu definieren.</span><span class="sxs-lookup"><span data-stu-id="9a111-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="9a111-115">Weitere Informationen finden Sie in [Hinzufügen eines Logos](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="9a111-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="9a111-116">Die Eigenschaft **Meine Kontolinks** kann verwendet werden, um Kontoseiten zu bestimmen, für die der Websitebesitzer Quicklinks in der Kopfzeile anzeigen möchte.</span><span class="sxs-lookup"><span data-stu-id="9a111-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="9a111-117">Module, die in einem Kopfzeilenmodul verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="9a111-117">Modules that are available within a header module</span></span>

<span data-ttu-id="9a111-118">Die folgenden Module können im Kopfzeilenmodul verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="9a111-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="9a111-119">**Navigationsmenü** – Das Navigationsmenü stellt die Kanalnavigationshierarchie und anderen statischen Navigationslinks dar.</span><span class="sxs-lookup"><span data-stu-id="9a111-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="9a111-120">Weitere Informationen finden Sie unter [Navigationsmenümodul](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="9a111-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="9a111-121">**Suche** – Das Suchmodul ermöglicht es Benutzern, Suchbegriffe einzugeben, sodass sie nach Produkten suchen können.</span><span class="sxs-lookup"><span data-stu-id="9a111-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="9a111-122">Die URL der Standardsuchseite und die Suchabfrageparameter müssen unter **Seiteneinstellungen \> Erweiterungen** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="9a111-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="9a111-123">Das Suchmodul verfügt über Eigenschaften, mit denen Sie die Suchschaltfläche oder -Bezeichnung nach Bedarf unterdrücken können.</span><span class="sxs-lookup"><span data-stu-id="9a111-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="9a111-124">Das Suchmodul unterstützt auch automatische Vorschlagsoptionen wie Produkt-, Keyword- und Kategoriesuchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="9a111-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="9a111-125">**Warenkorbsymbol** – Das Warenkorbsymbolmodul stellt das Warenkorbsymbol dar, das die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="9a111-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="9a111-126">Weitere Informationen finden Sie unter [Warenkorb-Symbolmodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="9a111-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

- <span data-ttu-id="9a111-127">**Site-Selektor** – Mit dem Site-Auswahlmodul können Benutzer verschiedene vordefinierte Sites durchsuchen, basierend auf Markt, Regionen und Gebietsschemas.</span><span class="sxs-lookup"><span data-stu-id="9a111-127">**Site selector** - The site selector module lets users browse across different predefined sites, based on market, regions, and locales.</span></span> <span data-ttu-id="9a111-128">Weitere Informationen finden Sie unter [Site-Auswahl-Modul](site-selector.md).</span><span class="sxs-lookup"><span data-stu-id="9a111-128">For more information, see [Site selector module](site-selector.md).</span></span>

- <span data-ttu-id="9a111-129">**Selektor speichern** – Das Store Selector-Modul kann in den Store Selector-Slot eines Header-Moduls aufgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="9a111-129">**Store selector** - The store selector module can be included in a header module's store selector slot.</span></span> <span data-ttu-id="9a111-130">Hier können Benutzer Geschäfte in der Nähe durchsuchen und finden.</span><span class="sxs-lookup"><span data-stu-id="9a111-130">It lets users browse and find nearby stores.</span></span> <span data-ttu-id="9a111-131">Benutzer können auch einen bevorzugten Store angeben.</span><span class="sxs-lookup"><span data-stu-id="9a111-131">Users can also specify a preferred store.</span></span> <span data-ttu-id="9a111-132">Dieser Store wird dann in der Kopfzeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9a111-132">That store will then be shown in the header.</span></span> <span data-ttu-id="9a111-133">Wenn das Store-Selector-Modul im Header-Modul enthalten ist, wird die **Modus** Eigenschaft auf **Store finden** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="9a111-133">When the store selector module is included in the header module, its **Mode** property must be set to **Find stores**.</span></span> <span data-ttu-id="9a111-134">Weitere Informationen finden Sie unter [Store-Auswahl-Modul](store-selector.md).</span><span class="sxs-lookup"><span data-stu-id="9a111-134">For more information, see [Store selector module](store-selector.md).</span></span>

> [!NOTE]
> - <span data-ttu-id="9a111-135">Hilfe für das Modul Warenkorbsymbol im Header-Modul finden Sie in Dynamics 365 Commerce Release 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="9a111-135">Support for using the cart icon module in header modules is available in the Dynamics 365 Commerce 10.0.11 release.</span></span>
> - <span data-ttu-id="9a111-136">Hilfe für das Modul Site-Selektor im Header-Modul finden Sie in Dynamics 365 Commerce Release 10.0.14.</span><span class="sxs-lookup"><span data-stu-id="9a111-136">Support for using the site selector module in header modules is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>
> - <span data-ttu-id="9a111-137">Hilfe für das Modul Store-Selektor im Header-Modul finden Sie in Dynamics 365 Commerce Release 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="9a111-137">Support for using the store selector module in header modules is available in the Dynamics 365 Commerce 10.0.15 release.</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="9a111-138">Erstellen eines Kopfzeilenfragment für eine Seite</span><span class="sxs-lookup"><span data-stu-id="9a111-138">Create a header fragment for a page</span></span>

<span data-ttu-id="9a111-139">Um ein neues Kopfzeilenfragment zu erstellen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="9a111-139">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="9a111-140">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a111-140">Go to **Fragments** , and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="9a111-141">Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Container** aus, geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-141">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="9a111-142">Wählen Sie den **Standardcontainer** -Slot aus und wählen Sie im Eigenschaftenfenster rechts die Eigenschaft **Breite** auf **Bildschirm ausfüllen**.</span><span class="sxs-lookup"><span data-stu-id="9a111-142">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="9a111-143">Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche ( **...** ) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="9a111-143">In the **Default container** slot, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9a111-144">Im Dialogfeld **Modul hinzufügen** wählen Sie die Module **Cookie-Zustimmung** , **Kopfzeile** und **Werbebanner** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-144">In the **Add Module** dialog box, select the **Cookie consent** , **Header** , and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="9a111-145">Im Eigenschaftenbereich des **Werbebanner** -Moduls wählen Sie **Nachricht hinzufügen** und dann **Nachricht** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-145">In the properties pane of the **Promo banner** module, select **Add Message** , and then select **Message**.</span></span>
1. <span data-ttu-id="9a111-146">Fügen Sie im Dialogfeld **Nachricht** dem Werbeinhalt Text und Links hinzu und wählen anschließend **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-146">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="9a111-147">Im Eigenschaftenbereich des **Cookie-Zustimmung** -Moduls fügen Sie der Datenschutzseite der Website Text und einen Link hinzu und konfigurieren diese.</span><span class="sxs-lookup"><span data-stu-id="9a111-147">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="9a111-148">Im Slot **Navigationsmenü** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen ( **...** ) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="9a111-148">In the **Navigation menu** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9a111-149">Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Navigationsmenü** und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="9a111-149">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9a111-150">Im Eigenschaftenbereich für das Navigationsmenümodul wählen Sie unter **Quelle für das Navigationsmenü** **Retail Server** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-150">In the property pane for the navigation menu module, under **Source for navigation menu** , select **Retail Server**.</span></span>
1. <span data-ttu-id="9a111-151">Im Eigenschaftenbereich für das Navigationsmenümodul wählen Sie unter **Statische Menüpunkte** **Menüpunkt hinzufügen** und dann **Menüpunkt** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-151">In the property pane for the navigation menu module, under **Static menu items** , select **Add Menu item** , and then select **Menu item**.</span></span> 
1. <span data-ttu-id="9a111-152">In dem **Menüpunkt** -Dialogfeld geben Sie unter **Menüelementtext** „Kontakt“ ein.</span><span class="sxs-lookup"><span data-stu-id="9a111-152">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="9a111-153">In dem **Menüpunkt** -Dialogfeld wählen Sie unter **Ziel des Menüelement-Links** **Link hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-153">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="9a111-154">Im Dialogfeld **Link hinzufügen** wählen Sie die URL für die „Kontakt“-Seite der Webite und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-154">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="9a111-155">Wählen Sie im Dialogfeld **Menüelement** die Option **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-155">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="9a111-156">Im Slot **Suchen** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen ( **...** ) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="9a111-156">In the **Search** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9a111-157">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Suchen** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-157">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9a111-158">Konfigurieren Sie im Eigenschaftenbereich für das Suchmodul die Eigenschaften des Navigationsmenümoduls nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="9a111-158">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="9a111-159">Im Slot **Einkaufswagensymbol** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen ( **...** ) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="9a111-159">In the **Cart icon** slot of the header module, select the ellipsis ( **...** ), and then select **Add Module**.</span></span>
1. <span data-ttu-id="9a111-160">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Einkaufswagen** -Modul und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="9a111-160">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="9a111-161">Konfigurieren Sie im Eigenschaftenbereich für das Warenkorbsymbol-Modult die Eigenschaften nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="9a111-161">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="9a111-162">Wenn das Warenkorbsymbol eine Warenkorbübersicht (auch als Minikorb bezeichnet) anzeigen soll, wenn Benutzer den Mauszeiger darüber halten, wählen Sie **Mini-Wagen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="9a111-162">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="9a111-163">Wählen Sie **Speichern** , wählen Sie **Bearbeiten beenden** , um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen** , um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="9a111-163">Select **Save** , select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="9a111-164">Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="9a111-164">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="9a111-165">Im Slot **Kopfzeile** wählen Sie das Modul **Standardseite** und fügen das Fußzeilenfragment hinzu, das Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="9a111-165">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="9a111-166">Wählen Sie **Speichern** , wählen Sie **Bearbeiten beenden** , um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen** , um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="9a111-166">Select **Save** , select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9a111-167">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9a111-167">Additional resources</span></span>

[<span data-ttu-id="9a111-168">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="9a111-168">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="9a111-169">Containermodul</span><span class="sxs-lookup"><span data-stu-id="9a111-169">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="9a111-170">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="9a111-170">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="9a111-171">Werbebannermodul</span><span class="sxs-lookup"><span data-stu-id="9a111-171">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="9a111-172">Navigationsmenümodul</span><span class="sxs-lookup"><span data-stu-id="9a111-172">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="9a111-173">Cookie-Einwilligung</span><span class="sxs-lookup"><span data-stu-id="9a111-173">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="9a111-174">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="9a111-174">Footer module</span></span>](author-footer-module.md)

[<span data-ttu-id="9a111-175">Siteauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="9a111-175">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="9a111-176">Shopauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="9a111-176">Store selector module</span></span>](store-selector.md)
