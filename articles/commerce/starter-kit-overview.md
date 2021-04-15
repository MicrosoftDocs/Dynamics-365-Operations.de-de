---
title: Informationen zur Modulbibliothek
description: Dieses Thema bietet einen Überblick über die Microsoft Dynamics 365 Commerce-Modulbibliothek.
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 76fd75c2ed9a3ba4728129b77a43b50267be3bf3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795332"
---
# <a name="module-library-overview"></a><span data-ttu-id="107a9-103">Informationen zur Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="107a9-103">Module library overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="107a9-104">Dieses Thema bietet einen Überblick über die Microsoft Dynamics 365 Commerce-Modulbibliothek.</span><span class="sxs-lookup"><span data-stu-id="107a9-104">This topic presents an overview of the Microsoft Dynamics 365 Commerce module library.</span></span>

<span data-ttu-id="107a9-105">Die Dynamics 365 Commerce-Modulbibliothek ist eine Sammlung von Modulen, mit denen eine E-Commerce-Website erstellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="107a9-105">The Dynamics 365 Commerce module library is a collection of modules that can be used to build an e-Commerce website.</span></span> <span data-ttu-id="107a9-106">Module besitzen sowohl Aspekte der Benutzeroberfläche (UI) als auch Aspekte des funktionalen Verhaltens.</span><span class="sxs-lookup"><span data-stu-id="107a9-106">Modules have both user interface (UI) aspects and functional behavior aspects.</span></span>

<span data-ttu-id="107a9-107">Die Module in der Modulbibliothek können mit Designs versehen werden, um ihr Erscheinungsbild zu ändern.</span><span class="sxs-lookup"><span data-stu-id="107a9-107">Themes can be applied to the modules in the module library to change their look and feel.</span></span> <span data-ttu-id="107a9-108">Die Designs verwenden Cascading Style Sheets (CSS).</span><span class="sxs-lookup"><span data-stu-id="107a9-108">The themes use Cascading Style Sheets (CSS).</span></span> <span data-ttu-id="107a9-109">Ein Design für eine fiktive E-Commerce-Site mit dem Namen „Fabrikam“ ist Teil der Modulbibliothek und kann als Referenz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="107a9-109">A theme for a fictitious e-Commerce site that is named "Fabrikam" is provided as part of the module library and can be used as a reference.</span></span>

## <a name="module-library-modules"></a><span data-ttu-id="107a9-110">Module der Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="107a9-110">Module library modules</span></span>

<span data-ttu-id="107a9-111">Die folgenden Modultypen sind in der Modulbibliothek enthalten:</span><span class="sxs-lookup"><span data-stu-id="107a9-111">The following types of modules are provided in the module library:</span></span>

- <span data-ttu-id="107a9-112">**Containermodul** – Ein Containermodul ist ein einfaches Modul, das als Host für andere Module fungiert.</span><span class="sxs-lookup"><span data-stu-id="107a9-112">**Container module** – A container module is a simple module that acts as a host for other modules.</span></span> <span data-ttu-id="107a9-113">Es steuert das Layout der darin enthaltenen Module.</span><span class="sxs-lookup"><span data-stu-id="107a9-113">It controls the layout of the modules that are inside it.</span></span>
- <span data-ttu-id="107a9-114">**Marketingmodule** – Zu den Marketingmodulen gehören Block-, Textblock-, Video-Player- und Karussell-Module.</span><span class="sxs-lookup"><span data-stu-id="107a9-114">**Marketing modules** – Marketing modules include content block, text block, video player, and carousel modules.</span></span> <span data-ttu-id="107a9-115">Alle diese Module können verwendet werden, um Inhalte zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="107a9-115">All these modules can be used to showcase content.</span></span> <span data-ttu-id="107a9-116">Sie können auf jede Seite gestellt werden und werden von Daten aus dem Content Management System (CMS) gesteuert.</span><span class="sxs-lookup"><span data-stu-id="107a9-116">They can be put on any page and are driven by data from the content management system (CMS).</span></span>
- <span data-ttu-id="107a9-117">**Kopf- und Fußzeilenmodule** – Kopf- und Fußzeilenmodule werden in den Kopf- und Fußzeilen aller Websiteseiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="107a9-117">**Header and footer modules** – Header and footer modules appear in the header and footer of all site pages.</span></span> <span data-ttu-id="107a9-118">Diese Module können nach Bedarf über Eigenschaften konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="107a9-118">These modules can be configured as required through properties.</span></span>
- <span data-ttu-id="107a9-119">**Suchmodule** – Produkte können mithilfe des Suchmoduls in der Kopfzeile gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="107a9-119">**Search modules** – Products can be discovered by using the search module in the header.</span></span> <span data-ttu-id="107a9-120">Suchergebnisse werden auf der Suchergebnisseite angezeigt.</span><span class="sxs-lookup"><span data-stu-id="107a9-120">Search results appear on the search results page.</span></span> <span data-ttu-id="107a9-121">Produkte können auch auf Kategorieseiten gefunden werden. Hierbei handelt es sich um dedizierte Seiten für jede Kategorie, die in der Kanalnavigationshierarchie unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="107a9-121">Products can also be discovered on category pages, which are dedicated pages for each category that is supported in the channel navigation hierarchy.</span></span> <span data-ttu-id="107a9-122">Darüber hinaus können mit Refiner-Modulen Suchergebnisse und Kategorieseiten weiter gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="107a9-122">In addition, refiner modules can be used to further filter results on search results and category pages.</span></span>
- <span data-ttu-id="107a9-123">**Produktdetailseitenmodule** – Produktdetailseiten verwenden mehrere Module, um Produktinformationen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="107a9-123">**Product details page modules** – Product details pages use several modules to show product information.</span></span> <span data-ttu-id="107a9-124">Mit dem Kauffeld-Modul können Kunden Produkte anzeigen und in den Einkaufskorb legen.</span><span class="sxs-lookup"><span data-stu-id="107a9-124">The buy box module lets customers view products and add them to the cart.</span></span> <span data-ttu-id="107a9-125">Andere Module, wie das Modul für technische Daten, zeigen die Produktdetails an.</span><span class="sxs-lookup"><span data-stu-id="107a9-125">Other modules, such as the tech specs module, show the product details.</span></span> <span data-ttu-id="107a9-126">Das Bewertungsmodul kann zum Anzeigen und Bereitstellen von Bewertungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="107a9-126">The ratings and reviews module can used to view and provide reviews.</span></span>
- <span data-ttu-id="107a9-127">**Modul Online kaufen, im Store abholen** – Das Modul Online kaufen, im Store abholen ist in Bing Maps integriert.</span><span class="sxs-lookup"><span data-stu-id="107a9-127">**Buy online pick up in store module** – The buy online pick up in store module is integrated with Bing Maps.</span></span> <span data-ttu-id="107a9-128">Es kann verwendet werden, um Geschäfte in der Nähe zu finden, in denen Kunden gekaufte Produkte abholen können.</span><span class="sxs-lookup"><span data-stu-id="107a9-128">It can be used to find nearby stores where customers can pick up products that they have purchased.</span></span>
- <span data-ttu-id="107a9-129">**Einkaufsmodule** – Zu den Einkaufsmodulen gehört das Einkaufskorbmodul, mit dem Sie Artikel in den Einkaufskorb legen können.</span><span class="sxs-lookup"><span data-stu-id="107a9-129">**Purchase modules** – Purchase modules include the cart module, which can be used to add items to the cart.</span></span> <span data-ttu-id="107a9-130">Das Auscheck-Modul erfasst die Versandadresse, die Lieferoptionen sowie die Informationen zu Geschenkkarte, Treueprogramm und Kreditkarte, sodass eine Bestellung verarbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="107a9-130">The checkout module captures the shipping address, delivery options, and gift card, loyalty program, and credit card information, so that an order can be processed.</span></span> <span data-ttu-id="107a9-131">Nachdem eine Bestellung aufgegeben wurde, kann das Bestellbestätigungsmodul verwendet werden, um die Bestätigungsdetails anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="107a9-131">After an order is placed, the order confirmation module can be used to show the confirmation details.</span></span>
- <span data-ttu-id="107a9-132">**Kontoverwaltungsmodul** – Mit dem Anmeldemodul können sich Kunden bei einem vorhandenen Konto anmelden, und mit dem Anmeldemodul können sie ein neues Konto erstellen.</span><span class="sxs-lookup"><span data-stu-id="107a9-132">**Account management modules** – The sign-in module lets customers sign in to an existing account, and the sign-up module lets them create a new account.</span></span> <span data-ttu-id="107a9-133">Nachdem ein Konto erstellt wurde, können mit dem Bestellverlaufsmodul die letzten Bestellungen und mit dem Bestelldetailmodul die Bestelldetails angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="107a9-133">After an account is created, the order history module can be used to view recent orders, and the order details module can be used to view order details.</span></span>
- <span data-ttu-id="107a9-134">**Empfehlungsmodul** – Empfehlungen werden mithilfe des Produktplatzierungs-Moduls angezeigt.</span><span class="sxs-lookup"><span data-stu-id="107a9-134">**Recommendations module** – Recommendations are shown by using the product placement module.</span></span> <span data-ttu-id="107a9-135">Dieses Modul unterstützt algorithmische und redaktionelle Listen, die auf jeder Seite angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="107a9-135">This module supports algorithmic and editorial lists that can be showcased on any page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="107a9-136">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="107a9-136">Additional resources</span></span>

[<span data-ttu-id="107a9-137">Containermodul</span><span class="sxs-lookup"><span data-stu-id="107a9-137">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="107a9-138">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="107a9-138">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="107a9-139">Einkaufskorbmodul</span><span class="sxs-lookup"><span data-stu-id="107a9-139">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="107a9-140">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="107a9-140">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="107a9-141">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="107a9-141">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="107a9-142">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="107a9-142">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="107a9-143">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="107a9-143">Footer module</span></span>](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]