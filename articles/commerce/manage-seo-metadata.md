---
title: Verwalten von SEO-Metadaten
description: In diesem Thema wird das Verwalten von SEO-Metadaten (Search Engine Optimization) in Microsoft Dynamics 365 Commerce beschrieben.
author: psimolin
manager: annbe
ms.date: 10/01/2019
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
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3ea06713af69659c205686a971393892fa584072
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945719"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="fa804-103">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="fa804-103">Manage SEO metadata</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="fa804-104">In diesem Thema wird das Verwalten von SEO-Metadaten (Search Engine Optimization) in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fa804-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="fa804-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="fa804-105">Overview</span></span>

<span data-ttu-id="fa804-106">SEO-Metadaten für eine Site können mithilfe von Site-Maps und Seitenmetadaten verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="fa804-106">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="fa804-107">Sitemaps</span><span class="sxs-lookup"><span data-stu-id="fa804-107">Site maps</span></span>

<span data-ttu-id="fa804-108">Eine Sitemap ist eine maschinenlesbare Liste der Seiten Ihrer Website im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="fa804-108">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="fa804-109">Sie soll von Suchmaschinen genutzt werden, damit sie bessere Suchergebnisse auf Ihrer Website bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="fa804-109">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="fa804-110">Sitemaps können manuell von Suchmaschinen erfasst oder in einer robots.txt-Datei veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="fa804-110">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="fa804-111">Dynamics 365 Commerce unterstützt die automatische Generierung von Sitemaps.</span><span class="sxs-lookup"><span data-stu-id="fa804-111">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="fa804-112">Siteübersichten werden automatisch aktualisiert, wenn die Seiten veröffentlicht bzw. zurückgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="fa804-112">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="fa804-113">Sitemap-Generierung aktivieren</span><span class="sxs-lookup"><span data-stu-id="fa804-113">Turn on site map generation</span></span>

1. <span data-ttu-id="fa804-114">Melden Sie sich beim Erstellungstool an.</span><span class="sxs-lookup"><span data-stu-id="fa804-114">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="fa804-115">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-115">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="fa804-116">Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-116">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="fa804-117">Stellen Sie sicher, dass die Option **Sitemaps aktiviert** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="fa804-117">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="fa804-118">Seitenmetadaten</span><span class="sxs-lookup"><span data-stu-id="fa804-118">Page metadata</span></span>

<span data-ttu-id="fa804-119">Mit Dynamics 365 Commerce können Sie SEO-Metadaten für einzelne Seiten verwalten.</span><span class="sxs-lookup"><span data-stu-id="fa804-119">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="fa804-120">Sie können diese Informationen im Abschnitt **SEO-Eigenschaften** eines Seitencontainers anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="fa804-120">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="fa804-121">Die folgenden SEO-Metadaten-Eigenschaften werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="fa804-121">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="fa804-122">Titel</span><span class="sxs-lookup"><span data-stu-id="fa804-122">Title</span></span>
- <span data-ttu-id="fa804-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa804-123">Description</span></span>
- <span data-ttu-id="fa804-124">SEO-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="fa804-124">SEO keywords</span></span>
- <span data-ttu-id="fa804-125">Aria-Labels</span><span class="sxs-lookup"><span data-stu-id="fa804-125">Aria labels</span></span>
- <span data-ttu-id="fa804-126">noindex</span><span class="sxs-lookup"><span data-stu-id="fa804-126">noindex</span></span>
- <span data-ttu-id="fa804-127">nofollow</span><span class="sxs-lookup"><span data-stu-id="fa804-127">nofollow</span></span>
- <span data-ttu-id="fa804-128">noarchive</span><span class="sxs-lookup"><span data-stu-id="fa804-128">noarchive</span></span>
- <span data-ttu-id="fa804-129">nocache</span><span class="sxs-lookup"><span data-stu-id="fa804-129">nocache</span></span>
- <span data-ttu-id="fa804-130">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="fa804-130">noOpenDirectoryProject</span></span>
- <span data-ttu-id="fa804-131">nosnippet</span><span class="sxs-lookup"><span data-stu-id="fa804-131">nosnippet</span></span>
- <span data-ttu-id="fa804-132">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="fa804-132">noImageIndex</span></span>
- <span data-ttu-id="fa804-133">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="fa804-133">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="fa804-134">Seitenmetadaten ändern</span><span class="sxs-lookup"><span data-stu-id="fa804-134">Modify page metadata</span></span>

<span data-ttu-id="fa804-135">Um Seitenmetadaten zu ändern, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-135">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="fa804-136">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-136">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="fa804-137">Wählen Sie im Navigationsbereich links **Seiten** aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-137">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="fa804-138">Wählen Sie die Startseite aus, um sie im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fa804-138">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="fa804-139">Wähle Sie im Aktivitätsbereich **Auschecken** aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-139">On the Action Pane, select **Check Out**.</span></span>
1. <span data-ttu-id="fa804-140">Erweitern Sie im Eigenschaftenbereich rechts **Standard-Metatags**.</span><span class="sxs-lookup"><span data-stu-id="fa804-140">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="fa804-141">Um ein neues Metatag hinzuzufügen, wählen Sie **Hinzufügen** aus und geben Sie den Tag dann im Feld ein.</span><span class="sxs-lookup"><span data-stu-id="fa804-141">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span>

    <span data-ttu-id="fa804-142">Um ein vorhandenes Metatag zu entfernen, wählen Sie das Papierkorb-Symbol rechts daneben aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-142">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>

1. <span data-ttu-id="fa804-143">Wählen Sie **Speichern** und dann **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-143">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="fa804-144">Geben Sie im Feld **Kommentare** **Aktualisierte Metatags** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-144">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="fa804-145">Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="fa804-145">Select **Preview** to preview your page.</span></span> <span data-ttu-id="fa804-146">Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="fa804-146">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="fa804-147">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="fa804-147">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fa804-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fa804-148">Additional resources</span></span>

[<span data-ttu-id="fa804-149">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="fa804-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="fa804-150">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="fa804-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="fa804-151">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="fa804-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="fa804-152">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="fa804-152">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="fa804-153">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="fa804-153">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="fa804-154">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="fa804-154">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="fa804-155">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="fa804-155">Verify page content accessibility</span></span>](verify-accessibility.md)
