---
title: Verwalten von SEO-Metadaten
description: In diesem Thema wird das Verwalten von SEO-Metadaten (Search Engine Optimization) in Microsoft Dynamics 365 Commerce beschrieben.
author: psimolin
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e03ef346df92a94b0a403f241d0f7d1f64fd210
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794210"
---
# <a name="manage-seo-metadata"></a><span data-ttu-id="8aad4-103">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="8aad4-103">Manage SEO metadata</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8aad4-104">In diesem Thema wird das Verwalten von SEO-Metadaten (Search Engine Optimization) in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="8aad4-104">This topic describes how to manage search engine optimization (SEO) metadata in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="8aad4-105">SEO-Metadaten für eine Site können mithilfe von Site-Maps und Seitenmetadaten verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="8aad4-105">SEO metadata for a site can be managed by using site maps and page metadata.</span></span>
    
## <a name="site-maps"></a><span data-ttu-id="8aad4-106">Sitemaps</span><span class="sxs-lookup"><span data-stu-id="8aad4-106">Site maps</span></span>

<span data-ttu-id="8aad4-107">Eine Sitemap ist eine maschinenlesbare Liste der Seiten Ihrer Website im XML-Format.</span><span class="sxs-lookup"><span data-stu-id="8aad4-107">A site map is a machine-readable list, in XML format, of the pages on your website.</span></span> <span data-ttu-id="8aad4-108">Sie soll von Suchmaschinen genutzt werden, damit sie bessere Suchergebnisse auf Ihrer Website bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="8aad4-108">It's intended to be consumed by search engines, so that they can provide better search results from your site.</span></span> <span data-ttu-id="8aad4-109">Sitemaps können manuell von Suchmaschinen erfasst oder in einer robots.txt-Datei veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="8aad4-109">Site maps can be manually ingested by search engines or published in a robots.txt file.</span></span>

<span data-ttu-id="8aad4-110">Dynamics 365 Commerce unterstützt die automatische Generierung von Sitemaps.</span><span class="sxs-lookup"><span data-stu-id="8aad4-110">Dynamics 365 Commerce supports automatic generation of site maps.</span></span> <span data-ttu-id="8aad4-111">Siteübersichten werden automatisch aktualisiert, wenn die Seiten veröffentlicht bzw. zurückgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="8aad4-111">Site maps are automatically updated when pages are published and unpublished.</span></span>

### <a name="turn-on-site-map-generation"></a><span data-ttu-id="8aad4-112">Sitemap-Generierung aktivieren</span><span class="sxs-lookup"><span data-stu-id="8aad4-112">Turn on site map generation</span></span>

1. <span data-ttu-id="8aad4-113">Melden Sie sich beim Erstellungstool an.</span><span class="sxs-lookup"><span data-stu-id="8aad4-113">Sign in to the authoring tool.</span></span>
1. <span data-ttu-id="8aad4-114">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-114">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8aad4-115">Wählen Sie im linken Navigationsbereich **Site-Verwaltung** aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="8aad4-116">Stellen Sie sicher, dass die Option **Sitemaps aktiviert** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8aad4-116">Make sure that the **Site maps enabled** option is turned on.</span></span>

## <a name="page-metadata"></a><span data-ttu-id="8aad4-117">Seitenmetadaten</span><span class="sxs-lookup"><span data-stu-id="8aad4-117">Page metadata</span></span>

<span data-ttu-id="8aad4-118">Mit Dynamics 365 Commerce können Sie SEO-Metadaten für einzelne Seiten verwalten.</span><span class="sxs-lookup"><span data-stu-id="8aad4-118">Dynamics 365 Commerce lets you manage SEO metadata for individual pages.</span></span> <span data-ttu-id="8aad4-119">Sie können diese Informationen im Abschnitt **SEO-Eigenschaften** eines Seitencontainers anzeigen und ändern.</span><span class="sxs-lookup"><span data-stu-id="8aad4-119">You can view and modify this information in the **SEO Properties** section of a page container.</span></span> <span data-ttu-id="8aad4-120">Die folgenden SEO-Metadaten-Eigenschaften werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="8aad4-120">The following SEO metadata properties are supported:</span></span>

- <span data-ttu-id="8aad4-121">Titel</span><span class="sxs-lookup"><span data-stu-id="8aad4-121">Title</span></span>
- <span data-ttu-id="8aad4-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8aad4-122">Description</span></span>
- <span data-ttu-id="8aad4-123">SEO-Schlüsselwörter</span><span class="sxs-lookup"><span data-stu-id="8aad4-123">SEO keywords</span></span>
- <span data-ttu-id="8aad4-124">Aria-Labels</span><span class="sxs-lookup"><span data-stu-id="8aad4-124">Aria labels</span></span>
- <span data-ttu-id="8aad4-125">noindex</span><span class="sxs-lookup"><span data-stu-id="8aad4-125">noindex</span></span>
- <span data-ttu-id="8aad4-126">nofollow</span><span class="sxs-lookup"><span data-stu-id="8aad4-126">nofollow</span></span>
- <span data-ttu-id="8aad4-127">noarchive</span><span class="sxs-lookup"><span data-stu-id="8aad4-127">noarchive</span></span>
- <span data-ttu-id="8aad4-128">nocache</span><span class="sxs-lookup"><span data-stu-id="8aad4-128">nocache</span></span>
- <span data-ttu-id="8aad4-129">noOpenDirectoryProject</span><span class="sxs-lookup"><span data-stu-id="8aad4-129">noOpenDirectoryProject</span></span>
- <span data-ttu-id="8aad4-130">nosnippet</span><span class="sxs-lookup"><span data-stu-id="8aad4-130">nosnippet</span></span>
- <span data-ttu-id="8aad4-131">noImageIndex</span><span class="sxs-lookup"><span data-stu-id="8aad4-131">noImageIndex</span></span>
- <span data-ttu-id="8aad4-132">unavailableAfter</span><span class="sxs-lookup"><span data-stu-id="8aad4-132">unavailableAfter</span></span>

### <a name="modify-page-metadata"></a><span data-ttu-id="8aad4-133">Seitenmetadaten ändern</span><span class="sxs-lookup"><span data-stu-id="8aad4-133">Modify page metadata</span></span>

<span data-ttu-id="8aad4-134">Um Seitenmetadaten zu ändern, führen Sie diese Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-134">To modify page metadata, follow these steps.</span></span>

1. <span data-ttu-id="8aad4-135">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-135">Under **Sites**, select the **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="8aad4-136">Wählen Sie im Navigationsbereich links **Seiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="8aad4-137">Wählen Sie die Startseite aus, um sie im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8aad4-137">Select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="8aad4-138">Wählen Sie in der Befehlsleiste **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-138">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="8aad4-139">Erweitern Sie im Eigenschaftenbereich rechts **Standard-Metatags**.</span><span class="sxs-lookup"><span data-stu-id="8aad4-139">In the properties pane on the right, expand **Default metatags**.</span></span>
1. <span data-ttu-id="8aad4-140">Um ein neues Metatag hinzuzufügen, wählen Sie **Hinzufügen** aus und geben Sie den Tag dann im Feld ein.</span><span class="sxs-lookup"><span data-stu-id="8aad4-140">To add a new metatag, select **Add**, and then enter the tag in the field.</span></span> <span data-ttu-id="8aad4-141">Um ein vorhandenes Metatag zu entfernen, wählen Sie das Papierkorb-Symbol rechts daneben aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-141">To remove an existing metatag, select the trash can symbol to the right of it.</span></span>
1. <span data-ttu-id="8aad4-142">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-142">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="8aad4-143">Geben Sie im Feld **Kommentare** **Aktualisierte Metatags** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-143">In the **Comments** field, enter **Updated metatags**, and then select **OK**.</span></span>
1. <span data-ttu-id="8aad4-144">Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8aad4-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="8aad4-145">Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="8aad4-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="8aad4-146">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="8aad4-146">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8aad4-147">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8aad4-147">Additional resources</span></span>

[<span data-ttu-id="8aad4-148">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="8aad4-148">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="8aad4-149">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="8aad4-149">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="8aad4-150">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="8aad4-150">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="8aad4-151">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="8aad4-151">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="8aad4-152">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="8aad4-152">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="8aad4-153">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="8aad4-153">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="8aad4-154">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="8aad4-154">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="8aad4-155">Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen</span><span class="sxs-lookup"><span data-stu-id="8aad4-155">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
