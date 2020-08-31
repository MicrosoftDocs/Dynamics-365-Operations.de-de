---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 05/28/2020
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
ms.openlocfilehash: e7dde3ba1ad375b309ae66cc6d31ccad85615e45
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686621"
---
# <a name="header-module"></a><span data-ttu-id="adc8b-103">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="adc8b-103">Header module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="adc8b-104">In diesem Thema werden Kopfzeilenmodule behandelt und die Erstellung von Kopfzeilen in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="adc8b-104">This topic covers header modules and describes how to create page headers in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="adc8b-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="adc8b-105">Overview</span></span>

<span data-ttu-id="adc8b-106">Im Dynamics 365 Commerce umfasst ein Seitenkopf mehrere Module, z. B. die Module Kopfzeile, Navigationsmenü, Suche, Werbebanner und Cookie-Einwilligung.</span><span class="sxs-lookup"><span data-stu-id="adc8b-106">In Dynamics 365 Commerce, a page header comprises multiple modules, such as the header, navigation menu, search, promo banner, and cookie consent modules.</span></span> 

<span data-ttu-id="adc8b-107">Das Kopfzeilenmodul enthält ein Site-Logo, Links zur Navigationshierarchie, Links zu anderen Seiten der Site, ein Warenkorbsymbol, ein Wunschliste-Symbol, Anmeldeoptionen und die Suchleiste.</span><span class="sxs-lookup"><span data-stu-id="adc8b-107">The header module includes a site logo, links to the navigation hierarchy, links to other pages on the site, a cart symbol, a wishlist symbol, sign-in options, and the search bar.</span></span> <span data-ttu-id="adc8b-108">Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site angezeigt wird (anders ausgedrückt für ein Desktopgerät oder ein mobiles Gerät).</span><span class="sxs-lookup"><span data-stu-id="adc8b-108">A header module is automatically optimized for the device that the site is being viewed on (in other words, for a desktop device or a mobile device).</span></span> <span data-ttu-id="adc8b-109">Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="adc8b-109">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

<span data-ttu-id="adc8b-110">Das folgende Bild zeigt ein Beispiel eines Kopfzeilenmoduls, das auf einer Startseite verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="adc8b-110">The following image shows an example of a header module on a home page.</span></span>

![Beispiel eines Kopfzeilenmoduls](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a><span data-ttu-id="adc8b-112">Eigenschaften eines Kopfmoduls</span><span class="sxs-lookup"><span data-stu-id="adc8b-112">Properties of a header module</span></span>

<span data-ttu-id="adc8b-113">Ein Kopfmodul unterstützt die Eigenschaften **Logo-Bild**, **Logo-Link** und **Meine Kontolinks**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-113">A header module supports **Logo image**, **Logo link**, and **My account links** properties.</span></span> 

<span data-ttu-id="adc8b-114">Die Eigenschaften **Logo-Bild** und **Logo-Link** werden verwendet, um ein Logo auf der Seite zu definieren.</span><span class="sxs-lookup"><span data-stu-id="adc8b-114">The **Logo image** and **Logo link** properties are used to define a logo on the page.</span></span> <span data-ttu-id="adc8b-115">Weitere Informationen finden Sie in [Hinzufügen eines Logos](add-logo.md).</span><span class="sxs-lookup"><span data-stu-id="adc8b-115">For more information, see [Add a logo](add-logo.md).</span></span> 

<span data-ttu-id="adc8b-116">Die Eigenschaft **Meine Kontolinks** kann verwendet werden, um Kontoseiten zu bestimmen, für die der Websitebesitzer Quicklinks in der Kopfzeile anzeigen möchte.</span><span class="sxs-lookup"><span data-stu-id="adc8b-116">The **My account links** property can be used to define account pages that the site owner wants to show quick links for in the header.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="adc8b-117">Module, die in einem Kopfzeilenmodul verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="adc8b-117">Modules that are available in a header module</span></span>

<span data-ttu-id="adc8b-118">Die folgenden Module können im Kopfzeilenmodul verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="adc8b-118">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="adc8b-119">**Navigationsmenü** – Das Navigationsmenü stellt die Kanalnavigationshierarchie und anderen statischen Navigationslinks dar.</span><span class="sxs-lookup"><span data-stu-id="adc8b-119">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="adc8b-120">Die Kanalnavigationshierarchie kann in Dynamics 365 Commerce konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="adc8b-120">The channel navigation hierarchy can be configured in Dynamics 365 Commerce.</span></span> <span data-ttu-id="adc8b-121">Das Navigationsmenü hat eine Eigenschaft **Navigationsquelle**, mit der die Retail Server-Navigationsmenüelemente und statische Menüelemente als Quelle angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="adc8b-121">The navigation menu has a **Navigation Source** property that is used to specify Retail Server navigation menu items and static menu items as a source.</span></span> <span data-ttu-id="adc8b-122">Wenn statische Menüelemente als Quelle angegeben werden, können relative Links zu anderen Seiten auf der Site bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="adc8b-122">If static menu items are specified as a source, relative links to other pages on the site can be provided.</span></span> <span data-ttu-id="adc8b-123">Konfigurierte Artikel werden dann als Kopfzeilennavigation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="adc8b-123">Configured items then appear as header navigation.</span></span> 

- <span data-ttu-id="adc8b-124">**Suche** – Das Suchmodul ermöglicht es Benutzern, Suchbegriffe einzugeben, sodass sie nach Produkten suchen können.</span><span class="sxs-lookup"><span data-stu-id="adc8b-124">**Search** – The search module lets users enter search terms to search for products.</span></span> <span data-ttu-id="adc8b-125">Die URL der Standardsuchseite und die Suchabfrageparameter müssen unter **Seiteneinstellungen \> Erweiterungen** angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="adc8b-125">The URL of the default search page and the search query parameters must be provided at **Site Settings \> Extensions**.</span></span> <span data-ttu-id="adc8b-126">Das Suchmodul verfügt über Eigenschaften, mit denen Sie die Suchschaltfläche oder -Bezeichnung nach Bedarf unterdrücken können.</span><span class="sxs-lookup"><span data-stu-id="adc8b-126">The search module has properties that let you suppress the search button or label as you require.</span></span> <span data-ttu-id="adc8b-127">Das Suchmodul unterstützt auch automatische Vorschlagsoptionen wie Produkt-, Keyword- und Kategoriesuchergebnisse.</span><span class="sxs-lookup"><span data-stu-id="adc8b-127">The search module also supports auto-suggest options, such as product, keyword, and category search results.</span></span>

- <span data-ttu-id="adc8b-128">**Warenkorbsymbol** – Das Warenkorbsymbolmodul stellt das Warenkorbsymbol dar, das die Anzahl der Artikel im Warenkorb zu einem bestimmten Zeitpunkt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="adc8b-128">**Cart icon** - The cart icon module represents the cart icon, which shows the number of items in the cart at any given time.</span></span> <span data-ttu-id="adc8b-129">Weitere Informationen finden Sie unter [Warenkorb-Symbolmodul](cart-icon-module.md).</span><span class="sxs-lookup"><span data-stu-id="adc8b-129">For more information, see [Cart icon module](cart-icon-module.md).</span></span>

## <a name="create-a-header-module-for-a-page"></a><span data-ttu-id="adc8b-130">Erstellen eines Kopfzeilenmoduls für eine Seite</span><span class="sxs-lookup"><span data-stu-id="adc8b-130">Create a header module for a page</span></span>

<span data-ttu-id="adc8b-131">Um ein neues Kopfzeilenmodul zu erstellen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="adc8b-131">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="adc8b-132">Wechseln Sie zu **Fragmente** und wählen Sie **Neu** aus, um ein neues Fragment zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="adc8b-132">Go to **Fragments**, and select **New** to create a new fragment.</span></span>
1. <span data-ttu-id="adc8b-133">Wählen Sie im Dialogfeld **Neues Seitenfragment** das Modul **Container** aus, geben Sie einen Namen für das Seitenfragment ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="adc8b-133">In the **New page fragment** dialog box, select the **Container** module, enter a name for the page fragment, and then select **OK**.</span></span>
1. <span data-ttu-id="adc8b-134">Wählen Sie den **Standardcontainer**-Slot aus und wählen Sie im Eigenschaftenfenster rechts die Option **Breite** aus, um den **Behälter zu füllen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-134">Select the **Default container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="adc8b-135">Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-135">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adc8b-136">Im Dialogfeld **Modul hinzufügen** wählen Sie die Module **Promotionsanzeige** und **Cookie-Zustimmung** und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="adc8b-136">In the **Add Module** dialog box, select the **Promo banner** and **Cookie consent** modules, and then select **OK**.</span></span>
1. <span data-ttu-id="adc8b-137">Wählen Sie im Slot **Standard-Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-137">In the **Default container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adc8b-138">Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="adc8b-138">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="adc8b-139">Wählen Sie den **Container**-Slot aus und wählen Sie im Eigenschaftenbereich rechts die Option **Breite** aus, um den **Behälter zu füllen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-139">Select the **Container** slot, and then, in the properties pane on the right, set the **Width** property to **Fill container**.</span></span>
1. <span data-ttu-id="adc8b-140">Wählen Sie im Slot **Container** die Ellipsen-Schaltfläche (**...**) und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-140">In the **Container** slot, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adc8b-141">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Kopfzeile** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="adc8b-141">In the **Add Module** dialog box, select the **Header** module, and then select **OK**.</span></span>
1. <span data-ttu-id="adc8b-142">Im Slot **Navigationsmenü** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-142">In the **Navigation menu** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adc8b-143">Im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Navigationsmenü** und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-143">In the **Add Module** dialog box, select the **Navigation menu** module, and then select **OK**.</span></span>
1. <span data-ttu-id="adc8b-144">Konfigurieren Sie im Eigenschaftenbereich für das Navigationsmenümodul die Eigenschaften des Navigationsmenümoduls nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="adc8b-144">In the property pane for the navigation menu module, configure the properties as needed.</span></span>
1. <span data-ttu-id="adc8b-145">Im Slot **Suchen** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-145">In the **Search** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adc8b-146">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Suchen** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="adc8b-146">In the **Add Module** dialog box, select the **Search** module, and then select **OK**.</span></span>
1. <span data-ttu-id="adc8b-147">Konfigurieren Sie im Eigenschaftenbereich für das Suchmodul die Eigenschaften des Navigationsmenümoduls nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="adc8b-147">In the property pane for the search module, configure the properties as needed.</span></span>
1. <span data-ttu-id="adc8b-148">Im Slot **Einkaufswagensymbol** wählen Sie das Kopfzeilenmodul, wählen die Ellipsen (**...**) und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-148">In the **Cart icon** slot of the header module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="adc8b-149">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Einkaufswagen**-Modul und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="adc8b-149">In the **Add Module** dialog box, select the **Cart icon** module, and then select **OK**.</span></span>
1. <span data-ttu-id="adc8b-150">Konfigurieren Sie im Eigenschaftenbereich für das Warenkorbsymbol-Modult die Eigenschaften nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="adc8b-150">In the property pane for the cart icon module, configure the properties as needed.</span></span> <span data-ttu-id="adc8b-151">Wenn das Warenkorbsymbol eine Warenkorbübersicht (auch als Minikorb bezeichnet) anzeigen soll, wenn Benutzer den Mauszeiger darüber halten, wählen Sie **Mini-Wagen anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="adc8b-151">If you want the cart icon to display a cart summary (also known as a mini cart) when users hover over it, select **Show mini cart**.</span></span>
1. <span data-ttu-id="adc8b-152">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um das Fragment einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="adc8b-152">Select **Save**, select **Finish editing** to check in the fragment, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="adc8b-153">Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="adc8b-153">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="adc8b-154">Im Slot **Kopfzeile** wählen Sie das Modul **Standardseite** und fügen das Fußzeilenfragment hinzu, das Sie erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="adc8b-154">In the **Header** slot of the **Default page** module, add the footer fragment that you created.</span></span>
1. <span data-ttu-id="adc8b-155">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Vorlage einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="adc8b-155">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="adc8b-156">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="adc8b-156">Additional resources</span></span>

[<span data-ttu-id="adc8b-157">Überblick über Starterkit</span><span class="sxs-lookup"><span data-stu-id="adc8b-157">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="adc8b-158">Containermodul</span><span class="sxs-lookup"><span data-stu-id="adc8b-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="adc8b-159">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="adc8b-159">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="adc8b-160">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="adc8b-160">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="adc8b-161">Symbol Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="adc8b-161">Cart icon module</span></span>](cart-icon-module.md)

[<span data-ttu-id="adc8b-162">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="adc8b-162">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="adc8b-163">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="adc8b-163">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="adc8b-164">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="adc8b-164">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="adc8b-165">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="adc8b-165">Footer module</span></span>](author-footer-module.md)
