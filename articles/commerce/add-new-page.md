---
title: Neue Seite hinzufügen
description: In diesem Thema wird beschrieben, wie Sie eine neue Websiteseite in Microsoft Dynamics 365 Commerce hinzufügen.
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
ms.openlocfilehash: 4a2ecc3ef3ff3f708cec50e42777b50ec4576e25
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5797550"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="abe63-103">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="abe63-103">Add a new site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="abe63-104">In diesem Thema wird beschrieben, wie Sie eine neue Websiteseite in Microsoft Dynamics 365 Commerce hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="abe63-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="abe63-105">Nachdem Sie Vorlagen und Fragmente für Ihre Site erstellt haben, besteht der nächste Schritt darin, die Seiten zu erstellen, von denen die Kategorien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="abe63-105">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="abe63-106">Um anzufangen, müssen Sie eine Vorlage oder ein Layout, einen Seitenname und eine URL Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="abe63-106">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="abe63-107">Vorlage oder Layout</span><span class="sxs-lookup"><span data-stu-id="abe63-107">Template or layout</span></span>

<span data-ttu-id="abe63-108">Sie können entweder eine ursprüngliche Vorlage oder ein Layout für die neue Seite nutzen.</span><span class="sxs-lookup"><span data-stu-id="abe63-108">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="abe63-109">Weitere Informationen finden Sie unter [Vorlagen und Layouts Überblick](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="abe63-109">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="abe63-110">Seitenname</span><span class="sxs-lookup"><span data-stu-id="abe63-110">Page name</span></span>

<span data-ttu-id="abe63-111">Der Seitenname muss für die Seite eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="abe63-111">The page name must be unique to your page.</span></span> <span data-ttu-id="abe63-112">Er sollte beschreibend sein, sodass Sie ihn einfach finden können und andere Personen wissen, für was die Seite ist.</span><span class="sxs-lookup"><span data-stu-id="abe63-112">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="abe63-113">Wählen Sie den Seitennamen sorgfältig aus, da sie später nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="abe63-113">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="abe63-114">Seiten-URL</span><span class="sxs-lookup"><span data-stu-id="abe63-114">Page URL</span></span>

<span data-ttu-id="abe63-115">Sie können die Option haben, eine URL für die neue Seite einzugeben.</span><span class="sxs-lookup"><span data-stu-id="abe63-115">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="abe63-116">Wenn Sie eine Seite erstellen, können Sie eine Zeichenfolge eingeben, die verwendet wird, um die URL zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="abe63-116">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="abe63-117">Diese Zeichenfolge ist als relative URL oder URL-Typ bekannt.</span><span class="sxs-lookup"><span data-stu-id="abe63-117">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="abe63-118">Eine vollständige URL wird anschließend auf Basis des URL-Typs generiert, und die neue Seite wird zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="abe63-118">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="abe63-119">Sie können den URL-Typ später ändern, bevor Sie die Seite veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="abe63-119">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="abe63-120">Weitere Informationen finden Sie unter [Erstellen einer URL-Seite](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="abe63-120">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="abe63-121">Dynamics 365 Commerce entkoppelt URLs und Inhalt.</span><span class="sxs-lookup"><span data-stu-id="abe63-121">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="abe63-122">Das bedeutet, eine Seite kann erstellt werden, die keiner URL zugeordnet ist, und eine URL kann erstellt werden, die keiner Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="abe63-122">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="abe63-123">Daher kann Inhalt-Auslagerung für eine URL erfolgen und erfordert keine Ausfallzeit und die Umleitungen sind einfacher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="abe63-123">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="abe63-124">Eine neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="abe63-124">Add a new page</span></span>

<span data-ttu-id="abe63-125">Um eine neue Seite Ihrer Site hinzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-125">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="abe63-126">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-126">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="abe63-127">Wählen Sie **Neue Seite** aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-127">Select **New Page**.</span></span>
1. <span data-ttu-id="abe63-128">Wählen Sie im Dialogfeld **Neue Seite** eine Vorlage und wählen dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="abe63-128">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="abe63-129">Wählen Sie im Feld **Seitenname** einen Seitennamen (z.B. **Meine neue Seite**).</span><span class="sxs-lookup"><span data-stu-id="abe63-129">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="abe63-130">Wählen Sie das Feld **URL** und geben Sei eine Zeichenfolge ein (URL-Typ) um die URL abzuschließen (beispielsweise **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="abe63-130">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="abe63-131">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="abe63-131">Select **OK**.</span></span> <span data-ttu-id="abe63-132">Der Seiteneditor wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="abe63-132">The page editor appears.</span></span> <span data-ttu-id="abe63-133">Beachten Sie, dass eine Kopf- und eine Fußzeile automatisch der Seite hinzugefügt werden, basierend auf der Vorlage, die Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="abe63-133">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="abe63-134">Auf dem Seitenüberblick wählen Sie den Slot (**Haupt**) und wählen die Ellipsen-Schaltfläche **...** und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="abe63-134">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="abe63-135">Wählen Sie **Container** und dann **OK** aus</span><span class="sxs-lookup"><span data-stu-id="abe63-135">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="abe63-136">Wählen Sie **Fluid Container** und wählen Sie dann die Ellipsen-Schaltfläche und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="abe63-136">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="abe63-137">Wählen Sie **Umfangreicher Inhaltsblock** und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-137">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="abe63-138">Wählen Sie **Umfangreicher Inhaltsblock** und wählen Sie dann die Ellipsen-Schaltfläche und wählen dann **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="abe63-138">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="abe63-139">Wählen Sie **Umfangreiches Inhaltsblockelement** und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-139">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="abe63-140">Im Eigenschaftenbereich auf der rechten Seite, wählen Sie, **Absatz** und dann geben Sie im Feld **Mein Prüftext** ein.</span><span class="sxs-lookup"><span data-stu-id="abe63-140">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="abe63-141">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-141">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="abe63-142">Geben Sie im Feld **Kommentare** **Neue Seite hinzufügen** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-142">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="abe63-143">Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="abe63-143">Select **Preview** to preview your page.</span></span> <span data-ttu-id="abe63-144">Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="abe63-144">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="abe63-145">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-145">Select **Publish**.</span></span>
1. <span data-ttu-id="abe63-146">Im Navigationspfad (Breadcrumbs) wählen Sie **Fabrikam** (oder den Namen der Site).</span><span class="sxs-lookup"><span data-stu-id="abe63-146">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="abe63-147">Wählen Sie im linken Navigationsbereich **URLs** aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-147">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="abe63-148">Suchen Sie Ihre URL und wählen Sie sie aus in der Liste (**mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="abe63-148">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="abe63-149">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="abe63-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="abe63-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="abe63-150">Additional resources</span></span>

[<span data-ttu-id="abe63-151">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="abe63-151">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="abe63-152">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="abe63-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="abe63-153">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="abe63-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="abe63-154">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="abe63-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="abe63-155">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="abe63-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="abe63-156">Kategoriezielseite erweitern</span><span class="sxs-lookup"><span data-stu-id="abe63-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="abe63-157">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="abe63-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="abe63-158">Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen</span><span class="sxs-lookup"><span data-stu-id="abe63-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
