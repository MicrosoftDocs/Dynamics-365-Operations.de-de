---
title: Bewertungs- und Prüfungsmodule
description: Dieses Thema umfasst Bewertungen und Rezensionsmodule, die auf den Produktdetailseiten in Microsoft Dynamics 365 Commerce verwendet werden.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 85fb1272103eed7d6e44635b7c20438471d96b34
ms.sourcegitcommit: 8028fbc5b9585e87d3331ea02577ff82ede090af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2020
ms.locfileid: "3817729"
---
# <a name="ratings-and-reviews-modules"></a><span data-ttu-id="309f4-103">Bewertungs- und Prüfungsmodule</span><span class="sxs-lookup"><span data-stu-id="309f4-103">Ratings and reviews modules</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="309f4-104">Dieses Thema behandelt Bewertungen und Rezensionsmodule, die auf den Produktdetailseiten (PDPs) in Microsoft Dynamics 365 Commerce verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="309f4-104">This topic covers ratings and reviews modules used on product details pages (PDPs) in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="309f4-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="309f4-105">Overview</span></span>

<span data-ttu-id="309f4-106">Bewertungen und Rezensionen auf E-Commerce-Websites helfen Kunden, sich über Produkte zu informieren, bevor sie eine Kaufentscheidung treffen, und sind auch ein Mechanismus zum Sammeln von Kundenfeedback zu Produkten.</span><span class="sxs-lookup"><span data-stu-id="309f4-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, and are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="309f4-107">Bewertungen werden in Produktlisteseiten, Kategorielistenseiten, Suchergebnisseiten und anderen Standortsseiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="309f4-107">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> 

<span data-ttu-id="309f4-108">Rating-Histogramme und Produktbesprechungen werden auf PDPs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="309f4-108">Ratings histograms and product reviews are shown on PDPs.</span></span> <span data-ttu-id="309f4-109">Eine Schaltfläche **Eine Bewertun schreiben** ermöglicht Kunden, Bewertungen und Prüfungen für ein Produkt senden.</span><span class="sxs-lookup"><span data-stu-id="309f4-109">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span> <span data-ttu-id="309f4-110">Diese PDP-Funktionen werden durch Bewertungen und Rezensionsmodule gesteuert.</span><span class="sxs-lookup"><span data-stu-id="309f4-110">These PDP features are controlled by ratings and review modules.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="309f4-111">Bewertungs- und Prüfungsmodule in PDPs</span><span class="sxs-lookup"><span data-stu-id="309f4-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="309f4-112">Drei Module zeigen die Zusammenfassungen der Beurteilungen und Prüfungen an auf PDPs:</span><span class="sxs-lookup"><span data-stu-id="309f4-112">Three modules show the ratings and reviews summary on PDPs:</span></span>
- <span data-ttu-id="309f4-113">Modul Bewertung schreiben</span><span class="sxs-lookup"><span data-stu-id="309f4-113">Write review module</span></span>
- <span data-ttu-id="309f4-114">Modul Produktbewertungsliste</span><span class="sxs-lookup"><span data-stu-id="309f4-114">Product reviews list module</span></span>
- <span data-ttu-id="309f4-115">Bewertungshistogrammmodul</span><span class="sxs-lookup"><span data-stu-id="309f4-115">Ratings histogram module</span></span>
 
<span data-ttu-id="309f4-116">Die folgende Abbildung zeigt, wie die Bewertungen und Module aussehen auf einer PDP.</span><span class="sxs-lookup"><span data-stu-id="309f4-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Bewertungs- und Prüfungsmodule in einer PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="309f4-118">Informationen darüber, wie PDP-Vorlagen und -Layouts optimiert werden, sodass Sie die Konfigurationen der Module für Beurteilungen und Prüfungen unter verschiedenen PDPs auf Ihrer E-Commerce-Webseite freigeben können, finden Sie unter. [Vorlagen und Layoutüberblick](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="309f4-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="309f4-119">Die folgende Abbildung zeigt, wie das Dialogfeld **Modul hinzufügen** Bewertungs- und Prüfungsmodule in Dynamics 365 Commerce darstellt.</span><span class="sxs-lookup"><span data-stu-id="309f4-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>
<span data-ttu-id="309f4-120">![Fügen Sie ein Moduldialogfeld hinzu](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span><span class="sxs-lookup"><span data-stu-id="309f4-120">![Add module dialog box](media/rnr-eCommerce-pdp-adding-rnr-modules.png)</span></span>

### <a name="write-review-module"></a><span data-ttu-id="309f4-121">Modul Bewertung schreiben</span><span class="sxs-lookup"><span data-stu-id="309f4-121">Write review module</span></span>

<span data-ttu-id="309f4-122">Das Modul Bewertung schreiben enhält eine Schaltfläche **Bewertung schreiben**, bei der sich Benutzer anmelden, eine Bewertung zuweisen und eine Überprüfung eines Produkts schreiben können.</span><span class="sxs-lookup"><span data-stu-id="309f4-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="309f4-123">Mit diesem Modul können Benutzer eine Bewertung oder Prüfung bearbeiten, die sie zuvor übermittelt haben.</span><span class="sxs-lookup"><span data-stu-id="309f4-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="309f4-124">Dieses Modul wird in der Regel über den Produktbewertungs-Histogramm- und Produktbewertungslistenmodulen auf einem PDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="309f4-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>
<span data-ttu-id="309f4-125">Die folgende Abbildung zeigt das Dialogfeld **Eine Bewertung schreiben**, das angezeigt wird, wenn ein Debitor **Eine Bewertung schreiben** auswählt.</span><span class="sxs-lookup"><span data-stu-id="309f4-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="309f4-126">Der Debitor kann dieses Dialogfeld verwenden, um eine Bewertung und eine Prüfung zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="309f4-126">The customer can use this dialog box to submit a rating and a review.</span></span>
<span data-ttu-id="309f4-127">![Dialogfeld zum Schreiben einer Rezension](media/rnr-eCommerce-write-review-module.png) Die folgende Tabelle zeigt die Eigenschaft des Rezensionsmoduls zum Schreiben, die im Autorentool konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="309f4-127">![Write a review dialog box](media/rnr-eCommerce-write-review-module.png) The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>
| <span data-ttu-id="309f4-128">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="309f4-128">Property name</span></span> | <span data-ttu-id="309f4-129">Wert</span><span class="sxs-lookup"><span data-stu-id="309f4-129">Value</span></span>        | <span data-ttu-id="309f4-130">Eigenschaftbeschreibung</span><span class="sxs-lookup"><span data-stu-id="309f4-130">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="309f4-131">Name</span><span class="sxs-lookup"><span data-stu-id="309f4-131">Name</span></span>          | <span data-ttu-id="309f4-132">Bewertung schreiben</span><span class="sxs-lookup"><span data-stu-id="309f4-132">Write review</span></span> | <span data-ttu-id="309f4-133">Der Name des Moduls Bewertung schreiben</span><span class="sxs-lookup"><span data-stu-id="309f4-133">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="309f4-134">Bewertungshistogrammmodul</span><span class="sxs-lookup"><span data-stu-id="309f4-134">Ratings histogram module</span></span>

<span data-ttu-id="309f4-135">Das Bewertungshistogrammmodul zeigt ein Bewertungshistogramm.</span><span class="sxs-lookup"><span data-stu-id="309f4-135">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="309f4-136">Dieses Modul wird zwischen dem Modul Bewertung schreiben und dem Produktbewertungslistenmodul auf einem PDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="309f4-136">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>
<span data-ttu-id="309f4-137">Das Bewertungshistogrammmodul erfordert keine Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="309f4-137">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="309f4-138">Sie müssen das Modul in der PDP-Vorlage nur hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="309f4-138">You just have to add the module in the PDP template.</span></span> <span data-ttu-id="309f4-139">Die folgende Abbildung zeigt, wie eine PDP-Vorlage in Dynamics 365 Commerce aussieht, wenn Prüfungs- und Bewertungsmodule zur Anzeige auf PDPs konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="309f4-139">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>
<span data-ttu-id="309f4-140">![PDP-Vorlage, wenn Bewertungen und Prüfungen für die Anzeige auf PDPs konfiguriert werden](media/rnr-eCommerce-pdp-reviews-modules.png)</span><span class="sxs-lookup"><span data-stu-id="309f4-140">![PDP template when ratings and reviews are configured for display on PDPs](media/rnr-eCommerce-pdp-reviews-modules.png)</span></span>

### <a name="product-reviews-list-module"></a><span data-ttu-id="309f4-141">Modul Produktbewertungsliste</span><span class="sxs-lookup"><span data-stu-id="309f4-141">Product reviews list module</span></span>

<span data-ttu-id="309f4-142">Das Produktprüfungs-Listenmodul zeigt eine Liste der Produktprüfungen zusammen mit Sortierung, Filter, und Paginierungsoptionen an.</span><span class="sxs-lookup"><span data-stu-id="309f4-142">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="309f4-143">Dieses wird normalerweise nach dem Bewertungshistogrammmodul auf einem PDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="309f4-143">This module typically appears after the ratings histogram module on a PDP.</span></span>
<span data-ttu-id="309f4-144">In der folgenden Tabelle wird die Eigenschaft für das Produktbewertungslistenmodul angezeigt, das im Erstellungstool konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="309f4-144">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="309f4-145">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="309f4-145">Property name</span></span>              | <span data-ttu-id="309f4-146">Wert</span><span class="sxs-lookup"><span data-stu-id="309f4-146">Value</span></span> | <span data-ttu-id="309f4-147">Eigenschaftbeschreibung</span><span class="sxs-lookup"><span data-stu-id="309f4-147">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="309f4-148">Auf jeder Seite angezeigte Bewertungen</span><span class="sxs-lookup"><span data-stu-id="309f4-148">Reviews shown on each page</span></span> | <span data-ttu-id="309f4-149">10</span><span class="sxs-lookup"><span data-stu-id="309f4-149">10</span></span>    | <span data-ttu-id="309f4-150">Die Anzahl der Bewertungen, die gleichzeitig auf einem PDP angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="309f4-150">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="309f4-151">Schaltflächen **Weiter** und **Vorherige** werden eingeschlossen, damit Benutzer die Seiten der Bewertungen durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="309f4-151">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="309f4-152">Bewertungshistogramm - Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="309f4-152">Ratings histogram – Summary view</span></span>

<span data-ttu-id="309f4-153">Das Produktprüfungs-Listenmodul enthält einen Slot, in dem Sie ein Bewertungshistogrammmodul hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="309f4-153">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="309f4-154">Die folgende Abbildung zeigt, wie Sie ein Bewertungshistogrammmodul im Produktprüfungs-Listenmodul in Dynamics 365 Commerce hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="309f4-154">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Das Hinzufügen eines Bewertungshistogrammmoduls in einem Produktbewertungslistenmodul](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="additional-resources"></a><span data-ttu-id="309f4-156">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="309f4-156">Additional resources</span></span>

[<span data-ttu-id="309f4-157">Übersicht über die Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="309f4-157">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="309f4-158">Containermodul</span><span class="sxs-lookup"><span data-stu-id="309f4-158">Container module</span></span>](add-container-module.md)

[<span data-ttu-id="309f4-159">Einkaufswagenmodul</span><span class="sxs-lookup"><span data-stu-id="309f4-159">Cart module</span></span>](add-cart-module.md)

[<span data-ttu-id="309f4-160">Auschecken-Modul</span><span class="sxs-lookup"><span data-stu-id="309f4-160">Checkout module</span></span>](add-checkout-module.md)

[<span data-ttu-id="309f4-161">Auftragsbestätigungsmodul</span><span class="sxs-lookup"><span data-stu-id="309f4-161">Order confirmation module</span></span>](order-confirmation-module.md)

[<span data-ttu-id="309f4-162">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="309f4-162">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="309f4-163">Fußzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="309f4-163">Footer module</span></span>](author-footer-module.md)
