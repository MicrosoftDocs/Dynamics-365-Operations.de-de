---
title: Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site
description: In diesem Thema werden Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Website von der Entwicklung bis zur Produktion behandelt.
author: psimolin
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c4d1a4a1b14f7af1db1c53bd9ee1993cc9187609
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254792"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="b9283-103">Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Site</span><span class="sxs-lookup"><span data-stu-id="b9283-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b9283-104">In diesem Thema werden Überlegungen zur Suchmaschinenoptimierung (SEO) für Ihre Website von der Entwicklung bis zur Produktion behandelt.</span><span class="sxs-lookup"><span data-stu-id="b9283-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="b9283-105">Eine Seite, die sich in der Entwicklung befindet</span><span class="sxs-lookup"><span data-stu-id="b9283-105">A site that is under development</span></span>

<span data-ttu-id="b9283-106">Während eine Website entwickelt wird, sollten alle Websiteseiten die folgende Bezeichnung haben: Die Metatags **NOINDEX** und **NOFOLLOW**, damit Suchmaschinen die Seiten nicht indizieren und Entwicklungsversionen Ihrer Website in ihrem Cache speichern.</span><span class="sxs-lookup"><span data-stu-id="b9283-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="b9283-107">Um diese Konfiguration durchzuführen, müssen Sie das Standard-Metatags-Modul zur Site-Seitenvorlage hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b9283-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="b9283-108">Die Standardeigenschaften für Metatags sind dann im Abschnitt SEO-Eigenschaften im Seiteneditor verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b9283-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="b9283-109">Mit diesen Eigenschaften können Sie die Metatags verwalten.</span><span class="sxs-lookup"><span data-stu-id="b9283-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="b9283-110">Langsame Einführung einer Website</span><span class="sxs-lookup"><span data-stu-id="b9283-110">Soft launch of a site</span></span>

<span data-ttu-id="b9283-111">Bei einer „langsamen Einführung“ wird eine Website einem begrenzten Publikum oder Markt zur Verfügung gestellt, bevor die vollständige Einführung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="b9283-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="b9283-112">Bei einer langsamen Einführung Ihrer Website sollten Sie die Metatags **NOINDEX** beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b9283-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="b9283-113">Auf diese Weise können Sie sicherstellen, dass die langsame Einführung auf das begrenzte Publikum beschränkt bleibt, das Sie erreichen möchten.</span><span class="sxs-lookup"><span data-stu-id="b9283-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="b9283-114">Eine Site, die in Produktion ist</span><span class="sxs-lookup"><span data-stu-id="b9283-114">A site that is in production</span></span>

<span data-ttu-id="b9283-115">Wenn eine Site in Produktion ist, sollten Sie sicherstellen, dass alle Site-Seiten korrekt mit Tags versehen sind.</span><span class="sxs-lookup"><span data-stu-id="b9283-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="b9283-116">Microsoft Dynamics 365 Commerce verwendet die für eine Seite eingegebenen Informationen, um alle SEO-Informationen auf dieser Seite zu rendern.</span><span class="sxs-lookup"><span data-stu-id="b9283-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="b9283-117">Die folgenden Module bieten diese Funktionalität: Kategorieseitenübersicht, Listenseitenübersicht und Produktseitenübersicht.</span><span class="sxs-lookup"><span data-stu-id="b9283-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="b9283-118">Um die Indizierung von Suchmaschinen zu optimieren, verwendet das Rendering-Framework beide Informationen aus den SEO-Eigenschaften, die in Dynamics 365 Commerce konfiguriert sind, und modulspezifische Informationen.</span><span class="sxs-lookup"><span data-stu-id="b9283-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="b9283-119">Für eine Site, die in Produktion ist, sollten Sie sicherstellen, dass die robots.txt-Datei die Indizierung Ihrer gesamten Site ermöglicht und Links zu Ihrem veröffentlichten Site-Map-Dokument enthält.</span><span class="sxs-lookup"><span data-stu-id="b9283-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="b9283-120">Sie sollten die Funktionalität zum Generieren der Sitemap unter **Website-Einstellungen \> Sitemaps aktiviert** aktivieren.</span><span class="sxs-lookup"><span data-stu-id="b9283-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="b9283-121">Seiten-SEO-Einstellungen für die interne Vorschau, begrenzte Zielgruppen und alle Zielgruppen</span><span class="sxs-lookup"><span data-stu-id="b9283-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="b9283-122">Da Dynamics 365 Commerce authentifizierte WYSIWYG-Vorschauen (What you see is what you get) in Visual Page Builder unterstützt, können Autoren ihren Seiteninhalt vorbereiten, ohne befürchten zu müssen, dass die Informationen für die Besucher der Website sichtbar werden.</span><span class="sxs-lookup"><span data-stu-id="b9283-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="b9283-123">Wenn eine Seite veröffentlicht werden soll, ihre Verfügbarkeit jedoch begrenzt sein muss, sollte sie das Meta-Tag **NOINDEX** aufweisen, damit sie nicht von Suchmaschinen indiziert wird.</span><span class="sxs-lookup"><span data-stu-id="b9283-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="b9283-124">Wenn die Seite dann für alle Zielgruppen bereit ist, sollten alle grundlegenden SEO-Metadaten vorhanden sein, um die Effizienz der Suchmaschinenindizierung zu maximieren.</span><span class="sxs-lookup"><span data-stu-id="b9283-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="b9283-125">Darüber hinaus sollte das Metatag **NOLIMIT** entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="b9283-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b9283-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b9283-126">Additional resources</span></span>

[<span data-ttu-id="b9283-127">Verwalten von e-Commerce Benutzern und Rollen</span><span class="sxs-lookup"><span data-stu-id="b9283-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="b9283-128">Hinzufügen von Skriptcode zu Standortseiten zur Unterstützung von Telemetrie</span><span class="sxs-lookup"><span data-stu-id="b9283-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="b9283-129">Verwalten der Inhaltssicherheitsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="b9283-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]