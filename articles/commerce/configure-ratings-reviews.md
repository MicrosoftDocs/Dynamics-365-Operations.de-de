---
title: Konfigurieren von Bewertungen und Prüfungen
description: In diesem Thema wird beschrieben, wie Sie Ihre E-Commerce-Webseite konfigurieren, um Beurteilungen und Bewertungen in Microsoft Dynamics 365 Commerce anzuzeigen.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5161755b9e15e93fbb5eeb6404ea0820f7068ea7
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796074"
---
# <a name="configure-ratings-and-reviews"></a><span data-ttu-id="759c2-103">Bewertungen und Prüfungen konfigurieren</span><span class="sxs-lookup"><span data-stu-id="759c2-103">Configure ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="759c2-104">In diesem Thema wird beschrieben, wie Sie Ihre E-Commerce-Webseite konfigurieren, um Beurteilungen und Bewertungen in Microsoft Dynamics 365 Commerce anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="759c2-104">This topic describes how to configure your e-Commerce site to show customer ratings and reviews in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="759c2-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="759c2-105">Overview</span></span>

<span data-ttu-id="759c2-106">Bewertungen und Rezensionen auf E-Commerce-Websites helfen den Kunden, sich über Produkte zu informieren, bevor sie eine Kaufentscheidung treffen, indem sie ihnen zeigen, was andere Kunden über diese Produkte denken.</span><span class="sxs-lookup"><span data-stu-id="759c2-106">Ratings and reviews on e-Commerce websites help customers learn about products before they make a purchase decision by showing them what other customers think about those products.</span></span> <span data-ttu-id="759c2-107">Für E-Commerce-Websites sind Bewertungen und Prüfungen auch ein Mechanismus für das Zusammenfassen des Kundenfeedbacks zu Produkten.</span><span class="sxs-lookup"><span data-stu-id="759c2-107">For e-Commerce websites, ratings and reviews are also a mechanism for collecting customer feedback about products.</span></span> 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a><span data-ttu-id="759c2-108">Konfigurieren einer Site, die Bewertungen und Prüfungen anzeigt</span><span class="sxs-lookup"><span data-stu-id="759c2-108">Configure a site to show ratings and reviews</span></span>

<span data-ttu-id="759c2-109">Konfigurationswerte von Beurteilungen und Prüfungen wie die Mandant-Kennung, Prüfung der Textlänge und Prüfung der Titellänge werden auf Sitebene konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="759c2-109">Configuration values for ratings and reviews, such as the tenant ID, review text length, and review title length, are configured at the site level.</span></span> 

<span data-ttu-id="759c2-110">Um eine Site zu konfigurieren, damit Bewertungen und Prüfungen angezeigt werden, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="759c2-110">To configure a site to show ratings and reviews, follow these steps.</span></span> 

1. <span data-ttu-id="759c2-111">Gehen Sie zu **Startseite \> Sites**.</span><span class="sxs-lookup"><span data-stu-id="759c2-111">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="759c2-112">Wählen Sie den Namen Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="759c2-112">Select the name of your site.</span></span> 
1. <span data-ttu-id="759c2-113">Gehen Sie zu **Site-Einstellungen \> Erweiterungen**.</span><span class="sxs-lookup"><span data-stu-id="759c2-113">Go to **Site settings \> Extensions**.</span></span> 
1. <span data-ttu-id="759c2-114">Geben Sie in das Feld **Bewertungstext maximale Länge** die maximale Anzahl von Zeichen ein, die ein Bewertungstext haben kann (z.B. **1000**).</span><span class="sxs-lookup"><span data-stu-id="759c2-114">In the **Review text max length** field, enter the maximum number of characters that review text can have (for example, **1000**).</span></span> 
1. <span data-ttu-id="759c2-115">Geben Sie in das Feld **Rezensionstitel maximale Länge** die maximale Anzahl von Zeichen ein, die ein Rezensionstitel haben kann (z.B. **55**).</span><span class="sxs-lookup"><span data-stu-id="759c2-115">In the **Review title max length** field, enter the maximum number of characters that review titles can have (for example, **55**).</span></span> 
1. <span data-ttu-id="759c2-116">Wählen Sie **Speichern und veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="759c2-116">Select **Save and Publish**.</span></span> 

<span data-ttu-id="759c2-117">Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="759c2-117">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurieren einer Site, die Bewertungen und Prüfungen anzeigt](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a><span data-ttu-id="759c2-119">Verknüpfen Sie eine Produktbewertung mit dem Bewertungsbereich auf einer PDP</span><span class="sxs-lookup"><span data-stu-id="759c2-119">Link a product rating to the Reviews section of a PDP</span></span>

<span data-ttu-id="759c2-120">Eine Produktbewertung wird unter dem Produkttitel oben auf der PDP angezeigt.</span><span class="sxs-lookup"><span data-stu-id="759c2-120">A product rating is shown below the product title at the top of PDP.</span></span> <span data-ttu-id="759c2-121">Die Produktbewertung kann so konfiguriert werden, dass diese mit dem Bereich **Bewertung** der gleichen PDP verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="759c2-121">The product rating can be configured so that it's linked to the **Reviews** section of the same PDP.</span></span> 

<span data-ttu-id="759c2-122">Wenn Sie eine Produktbewertung mit dem Abschnitt **Bewertung** des PDP bewerten, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="759c2-122">To link a product rating to the **Reviews** section of the PDP, follow these steps.</span></span>

1. <span data-ttu-id="759c2-123">Öffnen Sie die PDP-Vorlage.</span><span class="sxs-lookup"><span data-stu-id="759c2-123">Open the PDP template.</span></span> 
1. <span data-ttu-id="759c2-124">Gehen Sie zu **Containerfeld-Moduleinstellungen kaufen**.</span><span class="sxs-lookup"><span data-stu-id="759c2-124">Go to **Buy box container module settings**.</span></span>
1. <span data-ttu-id="759c2-125">Wählen Sie unter **Feld kaufen** die Option **Produktbewertungen** und anschließend das Kontrollkästchen **Verknüpfen des vollständigen Prüfungsmoduls**.</span><span class="sxs-lookup"><span data-stu-id="759c2-125">Under **Buy box**, select **Product ratings**, and then select the **Link the click to full reviews module** check box.</span></span>

<span data-ttu-id="759c2-126">Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="759c2-126">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Verknüpfen Sie eine Produktbewertung mit dem Bewertungsbereich auf einer PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a><span data-ttu-id="759c2-128">Konfigurieren Sie den Link für die Datenschutz- und Richtlinienseite</span><span class="sxs-lookup"><span data-stu-id="759c2-128">Configure the link for the privacy and policy page</span></span>

<span data-ttu-id="759c2-129">Um den Link für die Datenschutz- und Richtlinienseite zu konfigurieren, gehen Sie wie folgt vor.</span><span class="sxs-lookup"><span data-stu-id="759c2-129">To configure the link for the privacy and policy page, follow these steps.</span></span>

1. <span data-ttu-id="759c2-130">Gehen Sie zu **Startseite \> Sites**.</span><span class="sxs-lookup"><span data-stu-id="759c2-130">Go to **Home \> Sites**.</span></span>
1. <span data-ttu-id="759c2-131">Wählen Sie den Namen Ihrer Site.</span><span class="sxs-lookup"><span data-stu-id="759c2-131">Select the name of your site.</span></span> 
1. <span data-ttu-id="759c2-132">Gehen Sie zu **Site-Einstellungen \> Erweiterungen**.</span><span class="sxs-lookup"><span data-stu-id="759c2-132">Go to **Site settings \> Extensions**.</span></span>
1. <span data-ttu-id="759c2-133">Auf der Registerkarte **Arbeitspläne** unter **RNR-Datenschutz und Richtlinie**, wählen Sie **Fügen Sie einen Link hinzu** aus.</span><span class="sxs-lookup"><span data-stu-id="759c2-133">On the **Routes** tab, under **RNR Privacy and Policy**, select **Add a link**.</span></span> <span data-ttu-id="759c2-134">Wenn bereits ein Link eingegeben wurde und Sie diesen ersetzen möchten, wählen Sie den Link.</span><span class="sxs-lookup"><span data-stu-id="759c2-134">If a link is already entered, and you want to replace it, select the link.</span></span> 
1. <span data-ttu-id="759c2-135">Im Dialogfeld **Fügen Sie einen Link hinzu** wählen Sie den Link für die Datenschutzrichtlinienseite und wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="759c2-135">In the **Add a link** dialog box, select the link for the privacy and policy page, and then select **OK**.</span></span> 
1. <span data-ttu-id="759c2-136">Wählen Sie **Speichern und veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="759c2-136">Select **Save and Publish**.</span></span> 

<span data-ttu-id="759c2-137">Die folgende Abbildung zeigt, wie diese Kongiguration aussieht in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="759c2-137">The following illustration shows what this configuration looks like in Dynamics 365 Commerce.</span></span>

![Konfigurieren Sie den Link für die Datenschutz- und Richtlinienseite](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a><span data-ttu-id="759c2-139">Konfigurieren Sie Bewertungen und Rezensionsmodule auf den Produktdetailseiten</span><span class="sxs-lookup"><span data-stu-id="759c2-139">Configure ratings and reviews modules on product details pages</span></span>

<span data-ttu-id="759c2-140">Informationen zur Konfiguration von Bewertungen und Rezensionsmodulen auf den Produktdetailseiten finden Sie unter [Bewertungen und Rezensionsmodule](ratings-reviews-modules.md).</span><span class="sxs-lookup"><span data-stu-id="759c2-140">For information on configuring ratings and reviews modules on product details pages, see [Ratings and reviews modules](ratings-reviews-modules.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="759c2-141">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="759c2-141">Additional resources</span></span>

[<span data-ttu-id="759c2-142">Überblick über Bewertungen und Prüfungen</span><span class="sxs-lookup"><span data-stu-id="759c2-142">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="759c2-143">Verwenden von Bewertungen und Prüfungen abonnieren</span><span class="sxs-lookup"><span data-stu-id="759c2-143">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="759c2-144">Bewertungen und Prüfungen verwalten</span><span class="sxs-lookup"><span data-stu-id="759c2-144">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="759c2-145">Konfigurieren Sie die Bewertungen und Rezensionsmodule auf den Produktdetailseiten</span><span class="sxs-lookup"><span data-stu-id="759c2-145">Configure ratings and reviews modules on product details pages</span></span>](ratings-reviews-modules.md)

[<span data-ttu-id="759c2-146">Synchronisieren von Produktbewertungen in Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="759c2-146">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]