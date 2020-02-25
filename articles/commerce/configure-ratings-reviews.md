---
title: Konfigurieren von Bewertungen und Prüfungen
description: In diesem Thema wird beschrieben, wie Sie Ihre E-Commerce-Webseite konfigurieren, um Beurteilungen und Bewertungen in Microsoft Dynamics 365 Commerce anzuzeigen.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002196"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="3d9bb-103">Konfigurieren von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="3d9bb-103">Configure ratings and reviews</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="3d9bb-104">In diesem Thema wird beschrieben, wie Sie Ihre E-Commerce-Webseite konfigurieren, um Beurteilungen und Bewertungen in Microsoft Dynamics 365 Commerce anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="3d9bb-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="3d9bb-105">Overview</span></span>

<span data-ttu-id="3d9bb-106">Bewertungen und Prüfungen auf der E-Commerce-Website helfen Kunden, mehr über die Produkte zu erfahren, bevor Sie eine Einkaufentscheidung machen, indem angezeigt wird, was Kunden über diese Produkte denken.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision, by showing them what other customers think about those products.</span></span> <span data-ttu-id="3d9bb-107">Für E-Commerce-Websites sind Bewertungen und Prüfungen auch ein Mechanismus für das Zusammenfassen des Kundenfeedbacks zu Produkten.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

<span data-ttu-id="3d9bb-108">Bewertungen werden in Produktlisteseiten, Kategorielistenseiten, Suchergebnisseiten und anderen Standortsseiten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-108">Ratings are shown on product list pages, category list pages, search results pages, and other site pages.</span></span> <span data-ttu-id="3d9bb-109">Bewertungshistogramme und Produktprüfungen werden auf Produktdetailseiten (PDPs) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-109">Ratings histograms and product reviews are shown on product details pages (PDPs).</span></span> <span data-ttu-id="3d9bb-110">Eine Schaltfläche **Eine Bewertun schreiben** ermöglicht Kunden, Bewertungen und Prüfungen für ein Produkt senden.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-110">A **Write a review** button lets customers submit ratings and reviews for a product.</span></span>

## <a name="ratings-and-reviews-modules-on-pdps"></a><span data-ttu-id="3d9bb-111">Bewertungs- und Prüfungsmodule in PDPs</span><span class="sxs-lookup"><span data-stu-id="3d9bb-111">Ratings and reviews modules on PDPs</span></span> 

<span data-ttu-id="3d9bb-112">Drei Module zeigen die Zusammenfassungen der Beurteilungen und Prüfungen an auf PDPs:</span><span class="sxs-lookup"><span data-stu-id="3d9bb-112">Three modules show the ratings and reviews summary on PDPs:</span></span>

- <span data-ttu-id="3d9bb-113">Modul Bewertung schreiben</span><span class="sxs-lookup"><span data-stu-id="3d9bb-113">Write review module</span></span>
- <span data-ttu-id="3d9bb-114">Modul Produktbewertungsliste</span><span class="sxs-lookup"><span data-stu-id="3d9bb-114">Product reviews list module</span></span>
- <span data-ttu-id="3d9bb-115">Bewertungshistogrammmodul</span><span class="sxs-lookup"><span data-stu-id="3d9bb-115">Ratings histogram module</span></span>
 
<span data-ttu-id="3d9bb-116">Die folgende Abbildung zeigt, wie die Bewertungen und Module aussehen auf einer PDP.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-116">The following illustration shows what the ratings and reviews modules look like on a PDP.</span></span>

![Bewertungs- und Prüfungsmodule in einer PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> <span data-ttu-id="3d9bb-118">Informationen darüber, wie PDP-Vorlagen und -Layouts optimiert werden, sodass Sie die Konfigurationen der Module für Beurteilungen und Prüfungen unter verschiedenen PDPs auf Ihrer E-Commerce-Webseite freigeben können, finden Sie unter. [Vorlagen und Layoutüberblick](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3d9bb-118">For information about how to optimize PDP templates and layouts so that you can share the configurations for ratings and reviews modules among multiple PDPs on your e-Commerce site, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

<span data-ttu-id="3d9bb-119">Die folgende Abbildung zeigt, wie das Dialogfeld **Modul hinzufügen** Bewertungs- und Prüfungsmodule in Dynamics 365 Commerce darstellt.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-119">The following illustration shows how the **Add module** dialog box presents ratings and reviews modules in Dynamics 365 Commerce.</span></span>

![Fügen Sie ein Moduldialogfeld hinzu](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a><span data-ttu-id="3d9bb-121">Modul Bewertung schreiben</span><span class="sxs-lookup"><span data-stu-id="3d9bb-121">Write review module</span></span>

<span data-ttu-id="3d9bb-122">Das Modul Bewertung schreiben enhält eine Schaltfläche **Bewertung schreiben**, bei der sich Benutzer anmelden, eine Bewertung zuweisen und eine Überprüfung eines Produkts schreiben können.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-122">The write review module includes a **Write a review** button that lets users sign in, assign a rating, and write a review of a product.</span></span> <span data-ttu-id="3d9bb-123">Mit diesem Modul können Benutzer eine Bewertung oder Prüfung bearbeiten, die sie zuvor übermittelt haben.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-123">This module also lets users edit a rating or review that they previously submitted.</span></span> <span data-ttu-id="3d9bb-124">Dieses Modul wird in der Regel über den Produktbewertungs-Histogramm- und Produktbewertungslistenmodulen auf einem PDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-124">This module typically appears above the ratings histogram and product reviews list modules on a PDP.</span></span>

<span data-ttu-id="3d9bb-125">Die folgende Abbildung zeigt das Dialogfeld **Eine Bewertung schreiben**, das angezeigt wird, wenn ein Debitor **Eine Bewertung schreiben** auswählt.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-125">The following illustration shows the **Write a review** dialog box that appears when a customer selects **Write a review**.</span></span> <span data-ttu-id="3d9bb-126">Der Debitor kann dieses Dialogfeld verwenden, um eine Bewertung und eine Prüfung zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-126">The customer can use this dialog box to submit a rating and a review.</span></span>

![Schreiben Sie ein Bewertungsdialogfeld](media/rnr-eCommerce-write-review-module.png)

<span data-ttu-id="3d9bb-128">In der folgenden Tabelle wird die Eigenschaft für das Modul Bewertung schreiben angezeigt, die im Erstellungstool konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-128">The following table shows the write review module property that needs to be configured in the authoring tool.</span></span>

| <span data-ttu-id="3d9bb-129">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="3d9bb-129">Property name</span></span> | <span data-ttu-id="3d9bb-130">Wert</span><span class="sxs-lookup"><span data-stu-id="3d9bb-130">Value</span></span>        | <span data-ttu-id="3d9bb-131">Eigenschaftbeschreibung</span><span class="sxs-lookup"><span data-stu-id="3d9bb-131">Property description</span></span>                 |
|---------------|--------------|--------------------------------------|
| <span data-ttu-id="3d9bb-132">Name</span><span class="sxs-lookup"><span data-stu-id="3d9bb-132">Name</span></span>          | <span data-ttu-id="3d9bb-133">Bewertung schreiben</span><span class="sxs-lookup"><span data-stu-id="3d9bb-133">Write review</span></span> | <span data-ttu-id="3d9bb-134">Der Name des Moduls Bewertung schreiben</span><span class="sxs-lookup"><span data-stu-id="3d9bb-134">The name of the write review module.</span></span> |

### <a name="ratings-histogram-module"></a><span data-ttu-id="3d9bb-135">Bewertungshistogrammmodul</span><span class="sxs-lookup"><span data-stu-id="3d9bb-135">Ratings histogram module</span></span>

<span data-ttu-id="3d9bb-136">Das Bewertungshistogrammmodul zeigt ein Bewertungshistogramm.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-136">The ratings histogram module shows a ratings histogram.</span></span> <span data-ttu-id="3d9bb-137">Dieses Modul wird zwischen dem Modul Bewertung schreiben und dem Produktbewertungslistenmodul auf einem PDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-137">This module typically appears between the write review module and the product reviews list module on a PDP.</span></span>

<span data-ttu-id="3d9bb-138">Das Bewertungshistogrammmodul erfordert keine Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-138">The ratings histogram module requires no configuration.</span></span> <span data-ttu-id="3d9bb-139">Sie müssen das Modul in der PDP-Vorlage nur hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-139">You just have to add the module in the PDP template.</span></span> 

<span data-ttu-id="3d9bb-140">Die folgende Abbildung zeigt, wie eine PDP-Vorlage in Dynamics 365 Commerce aussieht, wenn Prüfungs- und Bewertungsmodule zur Anzeige auf PDPs konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-140">The following illustrations shows what a PDP template looks like in Dynamics 365 Commerce when ratings and reviews modules are configured for display on PDPs.</span></span>

![PDP-Vorlage, wenn Bewertungen und Prüfungen für die Anzeige auf PDPs konfiguriert werden](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a><span data-ttu-id="3d9bb-142">Modul Produktbewertungsliste</span><span class="sxs-lookup"><span data-stu-id="3d9bb-142">Product reviews list module</span></span>

<span data-ttu-id="3d9bb-143">Das Produktprüfungs-Listenmodul zeigt eine Liste der Produktprüfungen zusammen mit Sortierung, Filter, und Paginierungsoptionen an.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-143">The product reviews list module shows a list of product reviews together with sort, filter, and pagination options.</span></span> <span data-ttu-id="3d9bb-144">Dieses wird normalerweise nach dem Bewertungshistogrammmodul auf einem PDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-144">This module typically appears after the ratings histogram module on a PDP.</span></span>

<span data-ttu-id="3d9bb-145">In der folgenden Tabelle wird die Eigenschaft für das Produktbewertungslistenmodul angezeigt, das im Erstellungstool konfiguriert werden muss.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-145">The following table shows the product reviews list module properties that need to be configured in the authoring tool.</span></span>

| <span data-ttu-id="3d9bb-146">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="3d9bb-146">Property name</span></span>              | <span data-ttu-id="3d9bb-147">Wert</span><span class="sxs-lookup"><span data-stu-id="3d9bb-147">Value</span></span> | <span data-ttu-id="3d9bb-148">Eigenschaftbeschreibung</span><span class="sxs-lookup"><span data-stu-id="3d9bb-148">Property description</span></span> |
|----------------------------|-------| ---------------------|
| <span data-ttu-id="3d9bb-149">Auf jeder Seite angezeigte Bewertungen</span><span class="sxs-lookup"><span data-stu-id="3d9bb-149">Reviews shown on each page</span></span> | <span data-ttu-id="3d9bb-150">10</span><span class="sxs-lookup"><span data-stu-id="3d9bb-150">10</span></span>    | <span data-ttu-id="3d9bb-151">Die Anzahl der Bewertungen, die gleichzeitig auf einem PDP angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-151">The number of reviews that should be shown at a time on a PDP.</span></span> <span data-ttu-id="3d9bb-152">Schaltflächen **Weiter** und **Vorherige** werden eingeschlossen, damit Benutzer die Seiten der Bewertungen durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-152">**Next** and **Previous** buttons are included, so that users can move through the pages of reviews.</span></span> |

#### <a name="ratings-histogram--summary-view"></a><span data-ttu-id="3d9bb-153">Bewertungshistogramm - Zusammenfassungsansicht</span><span class="sxs-lookup"><span data-stu-id="3d9bb-153">Ratings histogram – Summary view</span></span>

<span data-ttu-id="3d9bb-154">Das Produktprüfungs-Listenmodul enthält einen Slot, in dem Sie ein Bewertungshistogrammmodul hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-154">The product reviews list module includes a slot where you can add a ratings histogram module.</span></span> <span data-ttu-id="3d9bb-155">Die folgende Abbildung zeigt, wie Sie ein Bewertungshistogrammmodul im Produktprüfungs-Listenmodul in Dynamics 365 Commerce hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-155">The following illustration shows how you can add a ratings histogram module in the product reviews list module in Dynamics 365 Commerce.</span></span>

![Das Hinzufügen eines Bewertungshistogrammmoduls in einem Produktbewertungslistenmodul](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="3d9bb-157">Konfigurieren einer Site, die Bewertungen und Prüfungen anzeigt</span><span class="sxs-lookup"><span data-stu-id="3d9bb-157">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="3d9bb-158">Konfigurationswerte von Beurteilungen und Prüfungen wie die Mandant-Kennung, Prüfung der Textlänge und Prüfung der Titellänge werden auf Sitebene konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-158">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="3d9bb-159">Um eine Site zu konfigurieren, damit Bewertungen und Prüfungen angezeigt werden, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-159">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="3d9bb-160">Gehen Sie zu **Startseite \> Sites**.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-160">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="3d9bb-161">Wählen Sie den Namen Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-161">Select the name of your site.</span></span> 
1. <span data-ttu-id="3d9bb-162">Gehen Sie zu **Siteverwaltung \> Erweiterbarkeit**.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-162">Go to **Site management \> Extensibility**.</span></span> 
1. <span data-ttu-id="3d9bb-163">Wählen Sie im Feld **Maximale Textlänge prüfen** geben Sie die maximale Anzahl von Zeichen ein, die der Prüfungstext haben darf (z.B. **1000**).</span><span class="sxs-lookup"><span data-stu-id="3d9bb-163">In the **Review Text Max Length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="3d9bb-164">Im Feld **Maximale Titellänge prüfen** geben Sie die maximale Anzahl von Zeichen ein, die der Titel haben darf (z.B. **55**).</span><span class="sxs-lookup"><span data-stu-id="3d9bb-164">In the **Review Title Max Length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="3d9bb-165">Wählen Sie **Speichern und veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-165">Select **Save and Publish**.</span></span> 

<span data-ttu-id="3d9bb-166">Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-166">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurieren einer Site, die Bewertungen und Prüfungen anzeigt](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="3d9bb-168">Verknüpfen Sie eine Produktbewertung mit dem Bewertungsbereich auf einer PDP</span><span class="sxs-lookup"><span data-stu-id="3d9bb-168">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="3d9bb-169">Eine Produktbewertung wird unter dem Produkttitel oben auf der PDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-169">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="3d9bb-170">Die Produktbewertung kann so konfiguriert werden, dass diese mit dem Bereich **Bewertung** der gleichen PDP verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-170">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="3d9bb-171">Wenn Sie eine Produktbewertung mit dem Abschnitt **Bewertung** des PDP bewerten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-171">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="3d9bb-172">Öffnen Sie die PDP-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-172">Open the PDP template.</span></span> 
1. <span data-ttu-id="3d9bb-173">Gehen Sie zu **Containerfeld-Moduleinstellungen kaufen**.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-173">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="3d9bb-174">Wählen Sie unter **Feld kaufen** die Option **Produktbewertungen** und anschließend das Kontrollkästchen **Verknüpfen des vollständigen Prüfungsmoduls**.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-174">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="3d9bb-175">Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-175">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Verknüpfen Sie eine Produktbewertung mit dem Bewertungsbereich auf einer PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="3d9bb-177">Konfigurieren Sie den Link für die Datenschutz- und Richtlinienseite</span><span class="sxs-lookup"><span data-stu-id="3d9bb-177">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="3d9bb-178">Um den Link für die Datenschutz- und Richtlinienseite zu konfigurieren, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-178">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="3d9bb-179">Gehen Sie zu **Startseite \> Sites**.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-179">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="3d9bb-180">Wählen Sie den Namen Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-180">Select the name of your site.</span></span> 
1. <span data-ttu-id="3d9bb-181">Gehen Sie zu **Siteverwaltung \> Erweiterbarkeit**</span><span class="sxs-lookup"><span data-stu-id="3d9bb-181">Go to **Site management \> Extensibility**</span></span>
1. <span data-ttu-id="3d9bb-182">Auf der Registerkarte **Arbeitspläne** unter **RNR-Datenschutz und Richtlinie**, wählen Sie **Fügen Sie einen Link hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-182">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="3d9bb-183">Wenn bereits ein Link eingegeben wurde und Sie diesen ersetzen möchten, wählen Sie den Link.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-183">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="3d9bb-184">Im Dialogfeld **Fügen Sie einen Link hinzu** wählen Sie den Link für die Datenschutzrichtlinienseite und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-184">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="3d9bb-185">Wählen Sie **Speichern und veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-185">Select **Save and Publish**.</span></span> 

<span data-ttu-id="3d9bb-186">Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3d9bb-186">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurieren Sie den Link für die Datenschutz- und Richtlinienseite](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a><span data-ttu-id="3d9bb-188">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3d9bb-188">Additional resources</span></span>

[<span data-ttu-id="3d9bb-189">Überblick über Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="3d9bb-189">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="3d9bb-190">Abonnieren zum Verwenden von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="3d9bb-190">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="3d9bb-191">Verwalten von Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="3d9bb-191">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="3d9bb-192">Synchronisieren von Produktbewertungen in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="3d9bb-192">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
