---
title: Kopfzeilenmodul
description: In diesem Thema werden Kopfzeilenmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: d393701dacb88ab03a4b56724d93c794da6bb5c8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697274"
---
# <a name="header-module"></a><span data-ttu-id="f17d7-103">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="f17d7-103">Header module</span></span>

<span data-ttu-id="f17d7-104">[!include [banner](includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span><span class="sxs-lookup"><span data-stu-id="f17d7-104">[!include [banner]includes/preview-banner.md)] [!include [banner](includes/banner.md)]</span></span>

<span data-ttu-id="f17d7-105">In diesem Thema werden Kopfzeilenmodule behandelt und deren Erstellung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f17d7-105">This topic covers header modules and describes how to create them in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f17d7-106">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f17d7-106">Overview</span></span>

<span data-ttu-id="f17d7-107">Ein Kopfmodul ist ein spezieller Container, der verwendet wird, um alle Module zu hosten, die in der Kopzeile auf der Seite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f17d7-107">A header module is a special container that is used to host all the modules that will be shown in a page's header.</span></span> <span data-ttu-id="f17d7-108">Beispielsweise kann es das Sitelogo, Links zur Navigationshierarchie, Links zu anderen Seiten auf der Site und die Suchenleiste umfassen.</span><span class="sxs-lookup"><span data-stu-id="f17d7-108">For example, it can include your site logo, links to the navigation hierarchy, links to other pages on the site, and the search bar.</span></span>

<span data-ttu-id="f17d7-109">Ein Kopfmodul wird automatisch für das Gerät optimiert, auf dem die Site anzgezeigt wird (z.B. Desktopgerät oder mobiles Gerät).</span><span class="sxs-lookup"><span data-stu-id="f17d7-109">A header module is automatically optimized for the device that the site is being viewed on (that is, a desktop device or a mobile device).</span></span> <span data-ttu-id="f17d7-110">Beispiel wird auf einem mobilen Gerät die Navigationsleiste in einer Schaltfläche **Menü** verringert (mitunter auch als *Hamburgermenü* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="f17d7-110">For example, on a mobile device, the navigation bar is collapsed into a **Menu** button (which is sometimes referred to as a *hamburger menu*).</span></span>

## <a name="properties-of-a-header"></a><span data-ttu-id="f17d7-111">Eigenschaften einer Kopfzeile</span><span class="sxs-lookup"><span data-stu-id="f17d7-111">Properties of a header</span></span>

<span data-ttu-id="f17d7-112">Wie die generischen Container unterstützt ein Kopfzeilenmodul die Eigenschaften für die **Überschrift** und die **Breite**.</span><span class="sxs-lookup"><span data-stu-id="f17d7-112">Like generic containers, a header module supports the **heading** and **width** properties.</span></span>

<span data-ttu-id="f17d7-113">Ein Kopfzeilenmodul hat mehrere Slots.</span><span class="sxs-lookup"><span data-stu-id="f17d7-113">A header module has multiple slots.</span></span> <span data-ttu-id="f17d7-114">Beispielsweise gibt es Slots für eine Informationsmeldung, ein Navigationsmenü, Logo, Suchleiste, Einkaufskorbsymbol, Wunschlistensymbol und Kontoinformationen.</span><span class="sxs-lookup"><span data-stu-id="f17d7-114">For example, there are slots for an informational message, navigation menu, logo, search bar, cart icon, wish list icon, and account information.</span></span> <span data-ttu-id="f17d7-115">Jeder Slot unterstützt ein bestimmtes Modulset.</span><span class="sxs-lookup"><span data-stu-id="f17d7-115">Each slot supports a specific set of modules.</span></span>

## <a name="modules-that-are-available-in-a-header-module"></a><span data-ttu-id="f17d7-116">Module, die in einem Kopfzeilenmodul verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="f17d7-116">Modules that are available in a header module</span></span>

<span data-ttu-id="f17d7-117">Die folgenden Module können im Kopfzeilenmodul verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="f17d7-117">The following modules can be used in a header module:</span></span>

- <span data-ttu-id="f17d7-118">**Navigationsmenü** – Das Navigationsmenü stellt die Kanalnavigationshierarchie und anderen statischen Navigationslinks dar.</span><span class="sxs-lookup"><span data-stu-id="f17d7-118">**Navigation menu** – The navigation menu represents the channel navigation hierarchy and other static navigation links.</span></span> <span data-ttu-id="f17d7-119">Die Kanalnavigationshierarchie kann in Dynamics 365 Retail konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f17d7-119">The channel navigation hierarchy can be configured in Dynamics 365 Retail.</span></span> <span data-ttu-id="f17d7-120">Konfigurierte Artikel werden dann als Kopfzeilennavigation angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f17d7-120">Configured items then appear as header navigation.</span></span> <span data-ttu-id="f17d7-121">Darüber hinaus können statische Navigationslinks konfiguriert werden und es können relative Links zu anderen Seiten auf der E-Commerce-Webseite bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="f17d7-121">In addition, static navigation links can be configured, and relative links to other pages on the e-Commerce site can be provided.</span></span> <span data-ttu-id="f17d7-122">Die Kopfzeile kann links, rechts oder in der Mitte ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="f17d7-122">The header itself can be aligned left, right, or center.</span></span>
- <span data-ttu-id="f17d7-123">**Einkaufswagensymbol** – Das Einkaufswagensymbol ist ein spezielles Symbol, das den Einkaufswagen darstellt.</span><span class="sxs-lookup"><span data-stu-id="f17d7-123">**Cart icon** – The cart icon is a special icon that represents the cart.</span></span> <span data-ttu-id="f17d7-124">Sie wird in der Kopfzeile dargestellt und zeigt die Anzahl der Element im Einkaufswagen.</span><span class="sxs-lookup"><span data-stu-id="f17d7-124">It's shown in the header and indicates the number of items in the cart.</span></span> <span data-ttu-id="f17d7-125">Ein Link zu der Einkaufswagenseite sollte das Einkaufswagensymbol begleiten, damit Kunden zur Einkaufswagenseite umgeleitet werden können, wenn sie mit dem Symbol interagieren.</span><span class="sxs-lookup"><span data-stu-id="f17d7-125">A link to the cart page should accompany the cart icon, so that customers can be redirected to the cart page when they interact with the icon.</span></span>
- <span data-ttu-id="f17d7-126">**Wunschlistensymbol** – Das Wunschlistensymbol wird in der Kopfzeile angezeigt und zeigt die Anzahl der Artikel an, die der Wunschliste des Kunden hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="f17d7-126">**Wish list icon** – The wish list icon is shown in the header and indicates the number of items that have been added to the customer's wish list.</span></span> <span data-ttu-id="f17d7-127">Ein Link zu der Wunschlistenseite begleitet dieses Symbol, so dass der Kunde auf die Wunschlistenseite umgeleitet werden kann, wenn er mit dem Symbol interagieren.</span><span class="sxs-lookup"><span data-stu-id="f17d7-127">A link to the wish list page should accompany this icon, so that customers can be redirected to the wish list page when they interact with the icon.</span></span>
- <span data-ttu-id="f17d7-128">**Anmeldungsmodul** – Das Anmeldungsmodul wird in der Kopfzeile angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f17d7-128">**Sign-in module** – The sign-in module is shown in the header.</span></span> <span data-ttu-id="f17d7-129">Sie ermöglicht es Kunden, sich entweder beim Konto anzumelden oder sich für ein Konto zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="f17d7-129">It lets customers either sign in to their account or sign up for an account.</span></span> <span data-ttu-id="f17d7-130">Wenn der Debitor bereits angemeldet ist, kann das Modul so konfiguriert werden, dass Links zur Kontoauftragsverlaufseite oder einer anderen Seite angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="f17d7-130">If the customer is already signed in, the module can be configured to show links to the account page, order history page, or another page.</span></span>
- <span data-ttu-id="f17d7-131">**Logomodul** – Dieses Modul enthält das Logos, das den Einzelhändler und die Marke darstellt.</span><span class="sxs-lookup"><span data-stu-id="f17d7-131">**Logo module** – This module shows the logo that represents the retailer and brand.</span></span> <span data-ttu-id="f17d7-132">Es ist ein Bild, das einen Link hat.</span><span class="sxs-lookup"><span data-stu-id="f17d7-132">It's an image that has a link.</span></span> <span data-ttu-id="f17d7-133">Der Link wird normalerweise so konfiguriert, dass er eine Umleitung zur Startseite enthält. Deshalb können Debitoren rasch von jeder beliebigen Seite aus auf die Startseite zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="f17d7-133">The link is typically configured so that it has a redirect to the home page, Therefore, customers can quickly return to the home page from any page on the site.</span></span>
- <span data-ttu-id="f17d7-134">**Warnung** – Eine Warnung wird in der Kopfzeile angezeigt und wird verwendet, um eine Inline-Meldung anzuzeigen, die auf alle Seiten der Site Geltung hat.</span><span class="sxs-lookup"><span data-stu-id="f17d7-134">**Alert** – An alert appears in the header and is used to show an inline message that applies to all pages on the site.</span></span> <span data-ttu-id="f17d7-135">Beispielsweise könnte eine Warnung eine Nachricht anzeigen wie „Jahresendverkauf endet in 2 Tagen“.</span><span class="sxs-lookup"><span data-stu-id="f17d7-135">For example, an alert might show a message such as "Annual sale ends in 2 days."</span></span>
- <span data-ttu-id="f17d7-136">**Suchenleiste** – Die Suchenleiste ermöglicht es Benutzern, Suchbegriffe einzugeben, sodass sie nach Produkten suchen können.</span><span class="sxs-lookup"><span data-stu-id="f17d7-136">**Search bar** – The search bar lets users enter search terms so that they can search for products.</span></span> <span data-ttu-id="f17d7-137">Das Modul muss mit der URL der Suchergebnisseite konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="f17d7-137">The module must be configured with the URL of the search results page.</span></span> <span data-ttu-id="f17d7-138">Der Abfragezeichenfolgenparameter kann konfiguriert werden (der Standardwert ist **„q“**).</span><span class="sxs-lookup"><span data-stu-id="f17d7-138">The query string parameter can be configured (the default value is **"q"**).</span></span> <span data-ttu-id="f17d7-139">Die Suchenleiste hat einen Slot mit automatischen Vorschlägen, in dem das Modul automatische Vorschläge hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f17d7-139">The search bar has an autosuggest slot where the autosuggest module should be added.</span></span>
- <span data-ttu-id="f17d7-140">**Automatische Vorschläge** – Das Modul automatische Vorschläge zeigt die automatisch vorgeschlagenen Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="f17d7-140">**Autosuggest** – The autosuggest module shows automatically suggested results.</span></span> <span data-ttu-id="f17d7-141">Die Ergebnisse können Schlüsselwörter, Produkte oder Kategorien sein, in denen Suchbegriffe gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="f17d7-141">These results can be keywords, products, or categories where the search term is found.</span></span>

## <a name="create-a-header-module"></a><span data-ttu-id="f17d7-142">Erstellen eines Kopfzeilenmoduls</span><span class="sxs-lookup"><span data-stu-id="f17d7-142">Create a header module</span></span>

<span data-ttu-id="f17d7-143">Um ein neues Kopfzeilenmodul zu erstellen, befolgen Sie diese Schritte.</span><span class="sxs-lookup"><span data-stu-id="f17d7-143">To create a header module, follow these steps.</span></span>

1. <span data-ttu-id="f17d7-144">Erstellen Sie ein Seitenfragment, das ein Kopfzeilenmodul enthält.</span><span class="sxs-lookup"><span data-stu-id="f17d7-144">Create a page fragment that includes a header module.</span></span>
1. <span data-ttu-id="f17d7-145">Fügen Sie Module den Slots im Kopfzeilenmodul hinzu.</span><span class="sxs-lookup"><span data-stu-id="f17d7-145">Add modules to the slots in the header module.</span></span>
1. <span data-ttu-id="f17d7-146">Aktualisieren Sie die Einstellungen für jedes Modul.</span><span class="sxs-lookup"><span data-stu-id="f17d7-146">Update the settings for each module.</span></span>
1. <span data-ttu-id="f17d7-147">Speichern Sie das Seitenfragment.</span><span class="sxs-lookup"><span data-stu-id="f17d7-147">Save the page fragment.</span></span> 
1. <span data-ttu-id="f17d7-148">Laden Sie die Seite hoch und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="f17d7-148">Check in the page, and publish it.</span></span>

<span data-ttu-id="f17d7-149">Um Sicherzustellen, dass eine Kopfzeile auf jeder Seite angezeigt wird, führen Sie die folgenden Schritte für jede Seitenvorlage aus, die für die Site erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="f17d7-149">To help guarantee that a header appears on every page, follow these steps on every page template that is created for the site.</span></span>

1. <span data-ttu-id="f17d7-150">Auf der Standardseite fügen Sie das Seitenfragment hinzu, das das Kopfzeilenmodul im Hauptslot enthält.</span><span class="sxs-lookup"><span data-stu-id="f17d7-150">On the default page, add the page fragment containing the header module to the header in the main slot.</span></span>
1. <span data-ttu-id="f17d7-151">Vorlage speichern.</span><span class="sxs-lookup"><span data-stu-id="f17d7-151">Save the template.</span></span> 
1. <span data-ttu-id="f17d7-152">Überprüfen Sie in die Vorlage, und veröffentlichen Sie sie.</span><span class="sxs-lookup"><span data-stu-id="f17d7-152">Check in the template, and publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f17d7-153">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f17d7-153">Additional resources</span></span>

[<span data-ttu-id="f17d7-154">Starterkit-Überblick</span><span class="sxs-lookup"><span data-stu-id="f17d7-154">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f17d7-155">Containermodul</span><span class="sxs-lookup"><span data-stu-id="f17d7-155">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="f17d7-156">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="f17d7-156">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="f17d7-157">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="f17d7-157">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="f17d7-158">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="f17d7-158">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="f17d7-159">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="f17d7-159">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="f17d7-160">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="f17d7-160">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f17d7-161">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="f17d7-161">Footer module</span></span>](author-footer-module.md)
