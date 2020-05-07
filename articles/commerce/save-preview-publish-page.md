---
title: Speichern, Vorschau und Veröffentlichung einer Seite
description: In diesem Thema wird beschrieben, wie eine Seite in Microsoft Dynamics 365 Commerce gespeichert, als Vorschau angezeigt und veröffentlicht wird.
author: psimolin
manager: annbe
ms.date: 04/14/2020
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
ms.openlocfilehash: e1e19594327c0042915bfae87f480434a7fcb159
ms.sourcegitcommit: 7a1d01122790b904e2d96a7ea9f1d003392358a6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/17/2020
ms.locfileid: "3269980"
---
# <a name="save-preview-and-publish-a-page"></a><span data-ttu-id="0a303-103">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="0a303-103">Save, preview, and publish a page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0a303-104">In diesem Thema wird beschrieben, wie eine Seite in Microsoft Dynamics 365 Commerce gespeichert, als Vorschau angezeigt und veröffentlicht wird.</span><span class="sxs-lookup"><span data-stu-id="0a303-104">This topic describes how to save, preview, and publish a page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="save-a-page"></a><span data-ttu-id="0a303-105">Speichern einer Seite</span><span class="sxs-lookup"><span data-stu-id="0a303-105">Save a page</span></span>

<span data-ttu-id="0a303-106">Um eine Seite zu speichern, müssen Sie sie für sich selbst auschecken und im Seiteneditor öffnen.</span><span class="sxs-lookup"><span data-stu-id="0a303-106">To save a page, you must have it checked out to yourself and open in the page editor.</span></span> <span data-ttu-id="0a303-107">Um eine Seite auszuchecken, wählen Sie in der Befehlsleiste **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-107">To check out a page, select **Edit** on the command bar.</span></span> <span data-ttu-id="0a303-108">Nach dem Bearbeiten einer Seite sollten Sie diese umgehend speichern, um sicherzustellen, dass Ihre Änderungen beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="0a303-108">After you've finished editing a page, you should immediately save it to ensure that your changes are stored.</span></span>

<span data-ttu-id="0a303-109">Wenn Sie eine Seite speichern, sind die Änderungen nur für Sie sichtbar.</span><span class="sxs-lookup"><span data-stu-id="0a303-109">When you save a page, the changes are visible only to you.</span></span> <span data-ttu-id="0a303-110">Der Speichervorgang dient hauptsächlich zum Speichern von Änderungen, während die Seite noch nicht zum Einchecken bereit ist.</span><span class="sxs-lookup"><span data-stu-id="0a303-110">The save operation is intended primarily to store changes while the page isn't yet ready to be checked in.</span></span> <span data-ttu-id="0a303-111">Nachdem Sie die Seite bearbeitet haben, wird empfohlen, sie einzuchecken, damit die Änderungen für andere sichtbar werden.</span><span class="sxs-lookup"><span data-stu-id="0a303-111">When you've finished modifying the page, we recommend that you check it in, so that the changes become visible to others.</span></span> <span data-ttu-id="0a303-112">Zu diesem Zeitpunkt kann die Seite auch von anderen Benutzern ausgecheckt werden, die sie ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="0a303-112">At that point, the page can also be checked out by other users who must modify it.</span></span>

## <a name="preview-a-page"></a><span data-ttu-id="0a303-113">Eine Seite als Vorschau anzeigen</span><span class="sxs-lookup"><span data-stu-id="0a303-113">Preview a page</span></span>

<span data-ttu-id="0a303-114">Das Erstellungstool bietet zwei Arten von Vorschaufunktionen: einen Vorschaubereich „What you see is what you get“ (WYSIWYG) im Seiteneditor und ein separates Vorschaufenster.</span><span class="sxs-lookup"><span data-stu-id="0a303-114">The authoring tool offers two kinds of preview features: a "what you see is what you get" (WYSIWYG) preview pane in the page editor and a separate preview window.</span></span>

<span data-ttu-id="0a303-115">Bei der Verwendung des Seiteneditors wird eine WYSIWYG-Vorschau (What you see is what you get) im mittleren Bereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0a303-115">While you're using the page editor, a "what you see is what you get" (WYSIWYG) preview appears in the center pane.</span></span> <span data-ttu-id="0a303-116">Diese Vorschau wird automatisch aktualisiert, wenn Sie die Seite speichern.</span><span class="sxs-lookup"><span data-stu-id="0a303-116">This preview is automatically updated whenever you save the page.</span></span> <span data-ttu-id="0a303-117">Sie können dies auch manuell aktualisieren, indem Sie **Aktualisieren** in der Befehlsleiste auswählen.</span><span class="sxs-lookup"><span data-stu-id="0a303-117">You can also manually update it by selecting **Refresh** on the command bar.</span></span> <span data-ttu-id="0a303-118">In der WYSIWYG-Vorschau wird die Seite so gerendert, wie sie den Benutzern der Site angezeigt wird. Darüber werden jedoch Autorenhilfen gerendert.</span><span class="sxs-lookup"><span data-stu-id="0a303-118">The WYSIWYG preview renders the page just as the site's users will see it, but authoring helpers are rendered on top of it.</span></span>

<span data-ttu-id="0a303-119">Wenn Sie die Seite geändert haben, möchten Sie möglicherweise eine Vorschau anzeigen, um zu sehen, was Kunden sehen werden.</span><span class="sxs-lookup"><span data-stu-id="0a303-119">When you've finished modifying the page, you might want to preview it to see what customers will see.</span></span> <span data-ttu-id="0a303-120">Um eine Seite als Vorschau anzuzeigen, wählen Sie **Vorschau** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-120">To preview a page, select **Preview** on the command bar.</span></span> <span data-ttu-id="0a303-121">Die Vorschau wird in einem separaten Browserfenster angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0a303-121">The preview will appear in a separate browser window.</span></span> <span data-ttu-id="0a303-122">Die Seite im Vorschaufenster wird so gerendert, wie es der Benutzer der Site sieht.</span><span class="sxs-lookup"><span data-stu-id="0a303-122">The page in the preview window is rendered just as the site's user will see it.</span></span> <span data-ttu-id="0a303-123">Sie können die Größe des Fensters ändern, um sicherzustellen, dass die reagierenden Module in allen Ansichtsports korrekt gerendert werden.</span><span class="sxs-lookup"><span data-stu-id="0a303-123">You can resize the window to make sure that responsive modules are correctly rendered in all view ports.</span></span>

> [!NOTE]
> <span data-ttu-id="0a303-124">Authentifizierung und korrekte Berechtigungen sind erforderlich, um eine Vorschau des unveröffentlichten Inhalts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0a303-124">Authentication and correct permissions are required to preview unpublished content.</span></span> <span data-ttu-id="0a303-125">Wenn Sie die URL der Vorschau für eine andere Person freigeben, muss diese Person über die richtigen Berechtigungen für den Zugriff auf den Inhalt verfügen.</span><span class="sxs-lookup"><span data-stu-id="0a303-125">Therefore, if you share the URL of the preview with someone, that person must have the correct permissions to access the content.</span></span>

## <a name="publish-a-page"></a><span data-ttu-id="0a303-126">Eine Seite veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="0a303-126">Publish a page</span></span>

<span data-ttu-id="0a303-127">Wenn Ihre Seite fertig ist, besteht der nächste Schritt darin, sie zu veröffentlichen, damit externe Benutzer den Inhalt anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="0a303-127">When your page is ready, the next step is to publish it, so that external users can view the content.</span></span> <span data-ttu-id="0a303-128">Bevor Sie eine Seite veröffentlichen können, müssen Sie sie durch Auswählen von **Beenden Sie die Bearbeitung** in der Befehlsleiste einchecken.</span><span class="sxs-lookup"><span data-stu-id="0a303-128">Before you can publish a page, you must check it in by selecting **Finish editing** on the command bar.</span></span>

<span data-ttu-id="0a303-129">Sie können Seiten entweder im Seiteninspektor oder im Seiteneditor veröffentlichen und deren Veröffentlichung aufheben.</span><span class="sxs-lookup"><span data-stu-id="0a303-129">You can publish and unpublish pages from either the page inspector or the page editor.</span></span> <span data-ttu-id="0a303-130">Der Seiteninspektor zeigt eine Liste der Seiten an und ermöglicht Massenvorgänge.</span><span class="sxs-lookup"><span data-stu-id="0a303-130">The page inspector shows a list of pages and allows for bulk operations.</span></span> <span data-ttu-id="0a303-131">Mit dem Seiteneditor können Sie nur die einzelne Seite, die dort geöffnet ist, veröffentlichen oder deren Veröffentlichung aufheben.</span><span class="sxs-lookup"><span data-stu-id="0a303-131">The page editor can be used to publish or unpublish only the single page that is open in it.</span></span>

<span data-ttu-id="0a303-132">Um eine oder mehrere Seiten im Seiteninspektor zu veröffentlichen, wählen Sie die Seiten aus, stellen Sie sicher, dass sie eingecheckt sind, und wählen Sie dann **Veröffentlichen** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-132">To publish one or more pages from the page inspector, select the pages, make sure that they are checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="0a303-133">Die Seiten werden veröffentlicht, und Sie erhalten eine Benachrichtigung über den Vorgang im Authoring-Tool.</span><span class="sxs-lookup"><span data-stu-id="0a303-133">The pages are published, and you receive a notification about the operation in the authoring tool.</span></span>

<span data-ttu-id="0a303-134">Um eine einzelne Seite aus dem Seiteneditor heraus zu veröffentlichen, verfahren Sie ähnlich.</span><span class="sxs-lookup"><span data-stu-id="0a303-134">To publish a single page from the page editor, the procedure is similar.</span></span> <span data-ttu-id="0a303-135">Stellen Sie, während die Seite im Seiteneditor geöffnet ist, sicher, dass sie eingecheckt wurde, und wählen Sie dann **Veröffentlichen** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-135">While the page is open in the page editor, make sure that it has been checked in, and then select **Publish** on the command bar.</span></span> <span data-ttu-id="0a303-136">Die Seite wird veröffentlicht und Sie erhalten eine Benachrichtigung über den Vorgang.</span><span class="sxs-lookup"><span data-stu-id="0a303-136">The page is published, and you receive a notification about the operation.</span></span>

<span data-ttu-id="0a303-137">Wenn Sie eine Seite veröffentlichen, wird nur der Seiteninhalt veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="0a303-137">When you publish a page, just the page content is published.</span></span> <span data-ttu-id="0a303-138">Sie und andere Benutzer können die Seite nur dann aufrufen und anzeigen, wenn ihr eine URL zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0a303-138">You and other users can go to the page and view it only after a URL is associated with it.</span></span> <span data-ttu-id="0a303-139">Die URL muss getrennt veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="0a303-139">The URL must be published separately.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0a303-140">Bevor Sie eine Seite veröffentlichen können, müssen alle Bilder oder Fragmente, auf die die Seite verweist, bereits veröffentlicht sein.</span><span class="sxs-lookup"><span data-stu-id="0a303-140">Before you can publish a page, any images or fragments that the page references must already be published.</span></span>

## <a name="save-preview-and-publish-a-home-page"></a><span data-ttu-id="0a303-141">Speichern, Vorschau und Veröffentlichen einer Startseite</span><span class="sxs-lookup"><span data-stu-id="0a303-141">Save, preview, and publish a home page</span></span>

<span data-ttu-id="0a303-142">Gehen Sie folgendermaßen vor, um eine Startseite zu speichern, in der Vorschau anzuzeigen und zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0a303-142">To save, preview, and publish a home page, follow these steps.</span></span>

1. <span data-ttu-id="0a303-143">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-143">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0a303-144">Wählen Sie im Navigationsbereich links **Seiten** aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-144">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="0a303-145">Suchen Sie die Startseite und wählen Sie sie aus, um sie im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0a303-145">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="0a303-146">Wählen Sie **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-146">Select **Edit**.</span></span>
1. <span data-ttu-id="0a303-147">Ändern Sie die Seite nach Bedarf.</span><span class="sxs-lookup"><span data-stu-id="0a303-147">Modify the page as you require.</span></span>
1. <span data-ttu-id="0a303-148">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-148">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="0a303-149">Geben Sie im Feld **Kommentare** eine Notiz zu den Änderungen ein, die Sie vorgenommen haben, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-149">In the **Comments** field, enter a note about the changes that you made, and then select **OK**.</span></span>
1. <span data-ttu-id="0a303-150">Wählen Sie **Vorschau** aus, um Ihre Seite in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0a303-150">Select **Preview** to preview your page.</span></span> <span data-ttu-id="0a303-151">Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="0a303-151">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="0a303-152">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-152">Select **Publish**.</span></span>

## <a name="publish-a-url"></a><span data-ttu-id="0a303-153">Eine URL veröffentlichen</span><span class="sxs-lookup"><span data-stu-id="0a303-153">Publish a URL</span></span>

<span data-ttu-id="0a303-154">Führen Sie folgende Schritte aus, um eine URL zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="0a303-154">To publish a URL, follow these steps.</span></span>

1. <span data-ttu-id="0a303-155">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-155">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="0a303-156">Wählen Sie im linken Navigationsbereich **URLs** aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-156">In the navigation pane on the left, select **URLs**.</span></span>
1. <span data-ttu-id="0a303-157">Suchen und wählen Sie die zu veröffentlichende URL aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-157">Find and select the URL to publish.</span></span>
1. <span data-ttu-id="0a303-158">Wählen Sie in der Befehlsleiste **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="0a303-158">On the command bar, select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a303-159">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0a303-159">Additional resources</span></span>

[<span data-ttu-id="0a303-160">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="0a303-160">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="0a303-161">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="0a303-161">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="0a303-162">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="0a303-162">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="0a303-163">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="0a303-163">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="0a303-164">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="0a303-164">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="0a303-165">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="0a303-165">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="0a303-166">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="0a303-166">Verify page content accessibility</span></span>](verify-accessibility.md)
