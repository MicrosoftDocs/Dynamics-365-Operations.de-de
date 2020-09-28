---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: eb440a8fb67888c9411ad5998fead4d00982b436
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761223"
---
# <a name="header-module"></a><span data-ttu-id="defe1-103">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="defe1-103">Header module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="defe1-104">In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="defe1-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="defe1-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="defe1-105">Overview</span></span>

<span data-ttu-id="defe1-106">In Dynamics 365 Commerce wird eine Seitenkopfzeile als Seitenfragment konfiguriert, das die Module Kopfzeile, Werbebanner und Cookie-Zustimmung enthält.</span><span class="sxs-lookup"><span data-stu-id="defe1-106">In Dynamics 365 Commerce, a page header is configured as a page fragment that includes the header, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="defe1-107">Das Kopfzeilenmodul enthält ein Site-Logo, Links zur Navigationshierarchie, Links zu anderen Seiten der Site, ein Warenkorbsymbolmodul, ein Wunschliste-Symbol, Anmeldeoptionen und die Suchleiste.</span><span class="sxs-lookup"><span data-stu-id="defe1-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart icon module, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="defe1-108">Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site angezeigt wird (anders ausgedrückt für ein Desktopgerät oder ein mobiles Gerät).</span><span class="sxs-lookup"><span data-stu-id="defe1-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="defe1-109">Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="defe1-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="defe1-110">Das folgende Bild zeigt ein Beispiel eines Kopfzeilenmoduls, das auf einer Startseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="defe1-110">The following image shows an example of a header module on a home page.</span></span>

![Beispiel eines Kopfzeilenmoduls](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="defe1-112">Eigenschaften eines Kopfmoduls</span><span class="sxs-lookup"><span data-stu-id="defe1-112">Properties of a header module</span></span>

<span data-ttu-id="defe1-113">Ein Kopfmodul unterstützt die Eigenschaften **Logo-Bild**, **Logo-Link** und **Meine Kontolinks**.</span><span class="sxs-lookup"><span data-stu-id="defe1-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="defe1-114">Die Eigenschaften **Logo-Bild** und **Logo-Link** werden verwendet, um ein Logo auf der Seite zu definieren.</span><span class="sxs-lookup"><span data-stu-id="defe1-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="defe1-115">Weitere Informationen finden Sie in [Hinzufügen eines Logos](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="defe1-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="defe1-116">Die Eigenschaft **Meine Kontolinks** kann verwendet werden, um Kontoseiten zu bestimmen, für die der Websitebesitzer Quicklinks in der Kopfzeile anzeigen möchte.</span><span class="sxs-lookup"><span data-stu-id="defe1-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-within-a-header-module"></a><span data-ttu-id="defe1-117">Module, die in einem Kopfzeilenmodul verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="defe1-117">Modules that are available within a header module</span></span>

<span data-ttu-id="defe1-118">Die folgenden Module können im Kopfzeilenmodul verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="defe1-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="defe1-119">**Navigationsmenü** – Das Navigationsmenü stellt die Kanalnavigationshierarchie und anderen statischen Navigationslinks dar.</span><span class="sxs-lookup"><span data-stu-id="defe1-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="defe1-120">Weitere Informationen finden Sie unter [Navigationsmenümodul](nav-menu-module.md).</span><span class="sxs-lookup"><span data-stu-id="defe1-120">For more information, see [Navigation menu module](nav-menu-module.md).</span></span>

- <span data-ttu-id="defe1-121">**Suche** – Das Suchmodul ermöglicht es Benutzern, Suchbegriffe einzugeben, sodass sie nach Produkten suchen können.</span><span class="sxs-lookup"><span data-stu-id="defe1-121">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="defe1-122">Die URL der Standardsuchseite und die Suchabfrageparameter müssen unter **Seiteneinstellungen \> Erweiterungen** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="defe1-122">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="defe1-123">Das Suchmodul verfügt über Eigenschaften, mit denen Sie die Suchschaltfläche oder -Bezeichnung nach Bedarf unterdrücken können.</span><span class="sxs-lookup"><span data-stu-id="defe1-123">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="defe1-124">Das Suchmodul unterstützt auch automatische Vorschlagsoptionen wie Produkt-, Keyword- und Kategoriesuchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="defe1-124">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="defe1-125">**Warenkorbsymbol** – Das Warenkorbsymbolmodul stellt das Warenkorbsymbol dar, das die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="defe1-125">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="defe1-126">Weitere Informationen finden Sie unter [Warenkorb-Symbolmodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="defe1-126">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-fragment-for-a-page"></a><span data-ttu-id="defe1-127">Erstellen eines Kopfzeilenfragment für eine Seite</span><span class="sxs-lookup"><span data-stu-id="defe1-127">Create a header fragment for a page</span></span>

<span data-ttu-id="defe1-128">Um ein neues Kopfzeilenfragment zu erstellen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="defe1-128">To create a header fragment, follow these steps.</span></span>

1. <span data-ttu-id="defe1-129">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="defe1-129">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="defe1-130">Wählen Sie im Dialogfeld **Neues Fragment** das Modul **Container** aus, geben Sie einen Namen für das Fragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-130">In the **New fragment** dialog box, select the **Container** module, enter a name for the fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="defe1-131">Wählen Sie den **Standardcontainer**-Slot aus und wählen Sie im Eigenschaftenfenster rechts die Eigenschaft **Breite** auf **Bildschirm ausfüllen**.</span><span class="sxs-lookup"><span data-stu-id="defe1-131">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill Screen**.</span></span>
1. <span data-ttu-id="defe1-132">Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="defe1-132">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="defe1-133">Im Dialogfeld **Modul hinzufügen** wählen Sie die Module **Cookie-Zustimmung**, **Kopfzeile** und **Werbebanner** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-133">In the **Add Module** dialog box, select the **Cookie consent**, **Header**, and **Promo banner** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="defe1-134">Im Eigenschaftenbereich des **Werbebanner**-Moduls wählen Sie **Nachricht hinzufügen**und dann **Nachricht** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-134">In the properties pane of the **Promo banner** module, select **Add Message**, and then select **Message**.</span></span>
1. <span data-ttu-id="defe1-135">Fügen Sie im Dialogfeld **Nachricht** dem Werbeinhalt Text und Links hinzu und wählen anschließend **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-135">In the **Message** dialog box, add text and links for the promotional content, and then select **OK**.</span></span>
1. <span data-ttu-id="defe1-136">Im Eigenschaftenbereich des **Cookie-Zustimmung**-Moduls fügen Sie der Datenschutzseite der Website Text und einen Link hinzu und konfigurieren diese.</span><span class="sxs-lookup"><span data-stu-id="defe1-136">In the properties pane of the **Cookie consent** module, add and configure text and a link to the site privacy page.</span></span>
1. <span data-ttu-id="defe1-137">Im Slot **Navigationsmenü** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="defe1-137">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="defe1-138">Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Navigationsmenü** und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="defe1-138">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="defe1-139">Im Eigenschaftenbereich für das Navigationsmenümodul wählen Sie unter **Quelle für das Navigationsmenü** **Retail Server** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-139">In the property pane for the navigation menu module, under **Source for navigation menu**, select **Retail Server**.</span></span>
1. <span data-ttu-id="defe1-140">Im Eigenschaftenbereich für das Navigationsmenümodul wählen Sie unter **Statische Menüpunkte** **Menüpunkt hinzufügen** und dann **Menüpunkt** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-140">In the property pane for the navigation menu module, under **Static menu items**, select **Add Menu item**, and then select **Menu item**.</span></span> 
1. <span data-ttu-id="defe1-141">In dem **Menüpunkt**-Dialogfeld geben Sie unter **Menüelementtext** „Kontakt“ ein.</span><span class="sxs-lookup"><span data-stu-id="defe1-141">In the **Menu item** dialog box, under **Menu Item Text** enter "Contact."</span></span>
1. <span data-ttu-id="defe1-142">In dem **Menüpunkt**-Dialogfeld wählen Sie unter **Ziel des Menüelement-Links** **Link hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-142">In the **Menu item** dialog box, under **Menu Item Link target** select **Add a link**.</span></span>
1. <span data-ttu-id="defe1-143">Im Dialogfeld **Link hinzufügen** wählen Sie die URL für die „Kontakt“-Seite der Webite und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-143">In the **Add a link** dialog box, select the URL for the site's "Contact" page, and then select **OK**.</span></span>  
1. <span data-ttu-id="defe1-144">Wählen Sie im Dialogfeld **Menüelement** die Option **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-144">In the **Menu item** dialog box, select **OK**.</span></span>
1. <span data-ttu-id="defe1-145">Im Slot **Suchen** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="defe1-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="defe1-146">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Suchen** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="defe1-147">Konfigurieren Sie im Eigenschaftenbereich für das Suchmodul die Eigenschaften des Navigationsmenümoduls nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="defe1-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="defe1-148">Im Slot **Einkaufswagensymbol** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="defe1-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="defe1-149">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Einkaufswagen**-Modul und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="defe1-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="defe1-150">Konfigurieren Sie im Eigenschaftenbereich für das Warenkorbsymbol-Modult die Eigenschaften nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="defe1-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="defe1-151">Wenn das Warenkorbsymbol eine Warenkorbübersicht (auch als Minikorb bezeichnet) anzeigen soll, wenn Benutzer den Mauszeiger darüber halten, wählen Sie **Mini-Wagen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="defe1-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="defe1-152">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="defe1-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="defe1-153">Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="defe1-153">To help ensure that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="defe1-154">Im Slot **Kopfzeile** wählen Sie das Modul **Standardseite** und fügen das Fußzeilenfragment hinzu, das Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="defe1-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="defe1-155">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="defe1-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="defe1-156">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="defe1-156">Additional resources</span></span>

[<span data-ttu-id="defe1-157">Überblick über das Starterkit</span><span class="sxs-lookup"><span data-stu-id="defe1-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="defe1-158">Containermodul</span><span class="sxs-lookup"><span data-stu-id="defe1-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="defe1-159">Modul für Einkaufswagensymbol</span><span class="sxs-lookup"><span data-stu-id="defe1-159">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="defe1-160">Werbebannermodul</span><span class="sxs-lookup"><span data-stu-id="defe1-160">Promo banner module</span></span>](add-alert.md)

[<span data-ttu-id="defe1-161">Navigationsmenümodul</span><span class="sxs-lookup"><span data-stu-id="defe1-161">Navigation Menu module</span></span>](nav-menu-module.md) 

[<span data-ttu-id="defe1-162">Cookie-Einwilligung</span><span class="sxs-lookup"><span data-stu-id="defe1-162">Cookie consent</span></span>](cookie-consent-module.md)

[<span data-ttu-id="defe1-163">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="defe1-163">Footer module</span></span>](author-footer-module.md)
