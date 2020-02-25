---
title: Neue Seite hinzufügen
description: In diesem Thema wird beschrieben, wie Sie eine neue Websiteseite in Microsoft Dynamics 365 Commerce hinzufügen.
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
ms.openlocfilehash: 68461f1f0be46f979a67e1806e03c02200cf61db
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3001345"
---
# <a name="add-a-new-site-page"></a><span data-ttu-id="60ecc-103">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="60ecc-103">Add a new site page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="60ecc-104">In diesem Thema wird beschrieben, wie Sie eine neue Websiteseite in Microsoft Dynamics 365 Commerce hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="60ecc-104">This topic describes how to add a new site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="60ecc-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="60ecc-105">Overview</span></span>

<span data-ttu-id="60ecc-106">Nachdem Sie Vorlagen und Fragmente für Ihre Site erstellt haben, besteht der nächste Schritt darin, die Seiten zu erstellen, von denen die Kategorien verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60ecc-106">After you've created templates and fragments for your site, the next step is to start to create pages that use them.</span></span> <span data-ttu-id="60ecc-107">Um anzufangen, müssen Sie eine Vorlage oder ein Layout, einen Seitenname und eine URL Seite auswählen.</span><span class="sxs-lookup"><span data-stu-id="60ecc-107">To get started, you must select a template or layout, a page name, and a page URL.</span></span>

## <a name="template-or-layout"></a><span data-ttu-id="60ecc-108">Vorlage oder Layout</span><span class="sxs-lookup"><span data-stu-id="60ecc-108">Template or layout</span></span>

<span data-ttu-id="60ecc-109">Sie können entweder eine ursprüngliche Vorlage oder ein Layout für die neue Seite nutzen.</span><span class="sxs-lookup"><span data-stu-id="60ecc-109">You can use either a template or a layout for your new page.</span></span> <span data-ttu-id="60ecc-110">Weitere Informationen finden Sie unter [Vorlagen und Layouts Überblick](templates-layouts-overview.md).</span><span class="sxs-lookup"><span data-stu-id="60ecc-110">For more information, see [Templates and layouts overview](templates-layouts-overview.md).</span></span>

## <a name="page-name"></a><span data-ttu-id="60ecc-111">Seitenname</span><span class="sxs-lookup"><span data-stu-id="60ecc-111">Page name</span></span>

<span data-ttu-id="60ecc-112">Der Seitenname muss für die Seite eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="60ecc-112">The page name must be unique to your page.</span></span> <span data-ttu-id="60ecc-113">Er sollte beschreibend sein, sodass Sie ihn einfach finden können und andere Personen wissen, für was die Seite ist.</span><span class="sxs-lookup"><span data-stu-id="60ecc-113">It should be descriptive, so that you can easily find it and other people know what the page is intended for.</span></span> <span data-ttu-id="60ecc-114">Wählen Sie den Seitennamen sorgfältig aus, da sie später nicht geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="60ecc-114">Choose the page name carefully, because it can't be changed later.</span></span>

## <a name="page-url"></a><span data-ttu-id="60ecc-115">Seiten-URL</span><span class="sxs-lookup"><span data-stu-id="60ecc-115">Page URL</span></span>

<span data-ttu-id="60ecc-116">Sie können die Option haben, eine URL für die neue Seite einzugeben.</span><span class="sxs-lookup"><span data-stu-id="60ecc-116">You can have the option to enter a URL for your new page.</span></span> <span data-ttu-id="60ecc-117">Wenn Sie eine Seite erstellen, können Sie eine Zeichenfolge eingeben, die verwendet wird, um die URL zu vervollständigen.</span><span class="sxs-lookup"><span data-stu-id="60ecc-117">When you create a page, you can enter a string that will be used to form a complete URL.</span></span> <span data-ttu-id="60ecc-118">Diese Zeichenfolge ist als relative URL oder URL-Typ bekannt.</span><span class="sxs-lookup"><span data-stu-id="60ecc-118">This string is known as a relative URL or a URL slug.</span></span> <span data-ttu-id="60ecc-119">Eine vollständige URL wird anschließend auf Basis des URL-Typs generiert, und die neue Seite wird zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="60ecc-119">A complete URL is then generated based on the URL slug, and the new page is assigned to it.</span></span> <span data-ttu-id="60ecc-120">Sie können den URL-Typ später ändern, bevor Sie die Seite veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="60ecc-120">You can change the URL slug later, before you publish the page.</span></span> <span data-ttu-id="60ecc-121">Weitere Informationen finden Sie unter [Erstellen einer URL-Seite](create-page-URL.md).</span><span class="sxs-lookup"><span data-stu-id="60ecc-121">For more information, see [Create a page URL](create-page-URL.md).</span></span>

> [!NOTE]
> <span data-ttu-id="60ecc-122">Dynamics 365 Commerce entkoppelt URLs und Inhalt.</span><span class="sxs-lookup"><span data-stu-id="60ecc-122">Dynamics 365 Commerce decouples URLs and content.</span></span> <span data-ttu-id="60ecc-123">Das bedeutet, eine Seite kann erstellt werden, die keiner URL zugeordnet ist, und eine URL kann erstellt werden, die keiner Seite zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="60ecc-123">In other words, a page can be created that isn't associated with an URL, and a URL can be created that isn't associated with a page.</span></span> <span data-ttu-id="60ecc-124">Daher kann Inhalt-Auslagerung für eine URL erfolgen und erfordert keine Ausfallzeit und die Umleitungen sind einfacher zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="60ecc-124">Therefore, content swapping can be done for a URL and doesn't require downtime, and redirects are easier to manage.</span></span>

## <a name="add-a-new-page"></a><span data-ttu-id="60ecc-125">Eine neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="60ecc-125">Add a new page</span></span>

<span data-ttu-id="60ecc-126">Um eine neue Seite Ihrer Site hinzufügen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-126">To add a new site page to your site, follow these steps.</span></span>

1. <span data-ttu-id="60ecc-127">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-127">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="60ecc-128">Wählen Sie **Neue Seite** aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-128">Select **New Page**.</span></span>
1. <span data-ttu-id="60ecc-129">Wählen Sie im Dialogfeld **Neue Seite** eine Vorlage und wählen dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="60ecc-129">In the **New Page** dialog box, select a template, and then select **OK**.</span></span>
1. <span data-ttu-id="60ecc-130">Wählen Sie im Feld **Seitenname** einen Seitennamen (z.B. **Meine neue Seite**).</span><span class="sxs-lookup"><span data-stu-id="60ecc-130">In the **Page Name** field, enter a page name (for example, **My New Page**).</span></span>
1. <span data-ttu-id="60ecc-131">Wählen Sie das Feld **URL** und geben Sei eine Zeichenfolge ein (URL-Typ) um die URL abzuschließen (beispielsweise **mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="60ecc-131">In the **URL** field, enter a string (URL slug) to complete the URL (for example, **mynewpage**).</span></span>
1. <span data-ttu-id="60ecc-132">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="60ecc-132">Select **OK**.</span></span> <span data-ttu-id="60ecc-133">Der Seiteneditor wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="60ecc-133">The page editor appears.</span></span> <span data-ttu-id="60ecc-134">Beachten Sie, dass eine Kopf- und eine Fußzeile automatisch der Seite hinzugefügt werden, basierend auf der Vorlage, die Sie ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="60ecc-134">Notice that a header and a footer are automatically added to the page, based on the template that you selected.</span></span>
1. <span data-ttu-id="60ecc-135">Auf dem Seitenüberblick wählen Sie den Slot (**Haupt**) und wählen die Ellipsen-Schaltfläche **...** und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="60ecc-135">In the page outline, select the **Main** slot, select the ellipsis button (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="60ecc-136">Wählen Sie **Container** und dann **OK** aus</span><span class="sxs-lookup"><span data-stu-id="60ecc-136">Select **Container**, and then select **OK**</span></span>
1. <span data-ttu-id="60ecc-137">Wählen Sie **Fluid Container**und wählen Sie dann die Ellipsen-Schaltfläche und wählen **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="60ecc-137">Select **Fluid Container**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="60ecc-138">Wählen Sie **Umfangreicher Inhaltsblock** und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-138">Select **Content Rich block**, and then select **OK**.</span></span>
1. <span data-ttu-id="60ecc-139">Wählen Sie **Umfangreicher Inhaltsblock**und wählen Sie dann die Ellipsen-Schaltfläche und wählen dann **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="60ecc-139">Select **Content Rich Block**, select the ellipsis button, and then select **Add Module**.</span></span>
1. <span data-ttu-id="60ecc-140">Wählen Sie **Umfangreiches Inhaltsblockelement** und wählen Sie **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-140">Select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="60ecc-141">Im Eigenschaftenbereich auf der rechten Seite, wählen Sie, **Absatz** und dann geben Sie im Feld **Mein Prüftext** ein.</span><span class="sxs-lookup"><span data-stu-id="60ecc-141">In the properties pane on the right, select **Paragraph**, and then, in the field, enter **My test text**.</span></span>
1. <span data-ttu-id="60ecc-142">Wählen Sie **Speichern** und dann **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-142">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="60ecc-143">Geben Sie im Feld **Kommentare** **Neue Seite hinzufügen** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-143">In the **Comments** field, enter **Added new page**, and then select **OK**.</span></span>
1. <span data-ttu-id="60ecc-144">Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="60ecc-144">Select **Preview** to preview your page.</span></span> <span data-ttu-id="60ecc-145">Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="60ecc-145">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="60ecc-146">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-146">Select **Publish**.</span></span>
1. <span data-ttu-id="60ecc-147">Im Navigationspfad (Breadcrumbs) wählen Sie **Fabrikam** (oder den Namen der Site).</span><span class="sxs-lookup"><span data-stu-id="60ecc-147">In the navigation path (breadcrumbs), select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="60ecc-148">Wählen Sie im linken Navigationsbereich **URLs** aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-148">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="60ecc-149">Suchen Sie Ihre URL und wählen Sie sie aus in der Liste (**mynewpage**).</span><span class="sxs-lookup"><span data-stu-id="60ecc-149">Find and select your URL (**mynewpage**) in the list.</span></span>
1. <span data-ttu-id="60ecc-150">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="60ecc-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="60ecc-151">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="60ecc-151">Additional resources</span></span>

[<span data-ttu-id="60ecc-152">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="60ecc-152">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="60ecc-153">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="60ecc-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="60ecc-154">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="60ecc-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="60ecc-155">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="60ecc-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="60ecc-156">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="60ecc-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="60ecc-157">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="60ecc-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="60ecc-158">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="60ecc-158">Verify page content accessibility</span></span>](verify-accessibility.md)
