---
title: Bestehende Seite einer Website ändern
description: In diesem Thema wird beschrieben, wie Sie eine vorhandene Websiteseite in Microsoft Dynamics 365 Commerce ändern.
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
ms.openlocfilehash: 50373d3681e269bf6164b2a425bbafebdd93d64f
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945696"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="b601f-103">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="b601f-103">Modify an existing site page</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="b601f-104">In diesem Thema wird beschrieben, wie Sie eine vorhandene Websiteseite in Microsoft Dynamics 365 Commerce ändern.</span><span class="sxs-lookup"><span data-stu-id="b601f-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="b601f-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="b601f-105">Overview</span></span>

<span data-ttu-id="b601f-106">Wenn Sie eine Seite ändern müssen, müssen Sie sie zunächst im Seiteneditor öffnen.</span><span class="sxs-lookup"><span data-stu-id="b601f-106">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="b601f-107">Gehen Sie zu der Site, die Ihre Seite enthält, und suchen Sie dann in der Liste der Seiten die gewünschte Seite.</span><span class="sxs-lookup"><span data-stu-id="b601f-107">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="b601f-108">Wenn Sie die Seite nicht finden können, können Sie die umfangreiche Suchfunktion des Erstellungstools verwenden.</span><span class="sxs-lookup"><span data-stu-id="b601f-108">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="b601f-109">Geben Sie entweder den genauen Seitennamen oder die ersten Buchstaben und dann ein Sternchen ein (\*).</span><span class="sxs-lookup"><span data-stu-id="b601f-109">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="b601f-110">Eine gefilterte Liste der Seiten wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b601f-110">A filtered list of pages appears.</span></span> <span data-ttu-id="b601f-111">Sie können diese Liste verwenden, um die gewünschte Seite zu finden.</span><span class="sxs-lookup"><span data-stu-id="b601f-111">You can use this list to find the page that you want.</span></span> <span data-ttu-id="b601f-112">Nachdem Sie die richtige Seite gefunden haben, wählen Sie den Seitennamen aus, um die Seite im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b601f-112">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="b601f-113">Wenn Ihre Seite im Seiteninspektor angezeigt wird, können Sie sie auswählen und auschecken, bevor Sie sie im Seiteneditor öffnen.</span><span class="sxs-lookup"><span data-stu-id="b601f-113">If your page is visible in the page inspector, you can select it and check it out before you open it in the page editor.</span></span> <span data-ttu-id="b601f-114">Auf diese Weise können Sie mehrere Seiten gleichzeitig auschecken.</span><span class="sxs-lookup"><span data-stu-id="b601f-114">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="b601f-115">Nachdem die Seite im Seiteneditor geöffnet wurde, müssen Sie sicherstellen, dass sie für Sie ausgecheckt ist.</span><span class="sxs-lookup"><span data-stu-id="b601f-115">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="b601f-116">Die Befehlsleiste im Erstellungstools ist dynamisch, kontextbezogen und statusabhängig.</span><span class="sxs-lookup"><span data-stu-id="b601f-116">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="b601f-117">Daher werden nur die Aktionen angezeigt, die Sie derzeit auf der Seite ausführen können.</span><span class="sxs-lookup"><span data-stu-id="b601f-117">Therefore, it shows only the actions that you can curently perform on the page.</span></span> <span data-ttu-id="b601f-118">Wenn die Seite beispielsweise nicht für Sie ausgecheckt wurde, werden die Schalflächen **Speichern** und **Einchecken** nicht in der Befehlsleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b601f-118">For example, if the page isn't checked out to you, the **Save** and **Check in** buttons don't appear on the command bar.</span></span> <span data-ttu-id="b601f-119">Der Status der Seite wird auch auf der rechten Seite des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b601f-119">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="b601f-120">Wenn die Seite noch nicht für Sie ausgecheckt wurde, wählen Sie **Auschecken** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-120">If the page isn't already checked out to you, select **Check out** on the command bar.</span></span> <span data-ttu-id="b601f-121">Die Befehlsleiste ändert sich, um den neuen Status der Seite widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="b601f-121">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="b601f-122">Sie erhalten auch eine Benachrichtigung, die besagt, dass die Seite für Sie ausgecheckt wurde.</span><span class="sxs-lookup"><span data-stu-id="b601f-122">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="b601f-123">Der nächste Schritt besteht darin, Ihre tatsächlichen Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="b601f-123">The next step is to make your actual changes.</span></span> <span data-ttu-id="b601f-124">Häufig verwenden Sie die Seitengliederungsstruktur auf der linken Seite, um das zu ändernde Modul zu suchen und auszuwählen, und nehmen dann im Eigenschaftsfenster auf der rechten Seite Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="b601f-124">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="b601f-125">Ihre Änderung kann jedoch manchmal das Hinzufügen oder Entfernen von Modellen oder Fragmenten umfassen.</span><span class="sxs-lookup"><span data-stu-id="b601f-125">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="b601f-126">Um ein Fragment oder Modul hinzuzufügen, suchen Sie in der Seitenstruktur den Slot, dem Sie das Modul oder Fragment hinzufügen möchten, und klicken Sie dann auf die Schaltfläche mit den Auslassungspunkten (**...**) für diesen Slot.</span><span class="sxs-lookup"><span data-stu-id="b601f-126">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="b601f-127">Ein Menü mit Befehlen zum Hinzufügen eines Moduls oder Fragments wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b601f-127">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="b601f-128">Um ein Modul oder Fragment zu entfernen, suchen Sie es und wählen Sie es in der Seitenstruktur aus, klicken Sie auf die Schaltfläche mit den Auslassungspunkten und wählen Sie dann den Befehl zum Löschen des Moduls oder Fragments aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-128">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="b601f-129">Sie können auch die Eigenschaften für jedes Modul anzeigen und bearbeiten, das in der Vorschau „What You See Is What You Get“ (WYSIWYG) angezeigt wird, indem Sie es direkt auswählen.</span><span class="sxs-lookup"><span data-stu-id="b601f-129">You can also view and edit the properties for any module that is visible in the "what you see is what you get" (WYSIWYG) preview by selecting it directly.</span></span>

<span data-ttu-id="b601f-130">Nachdem Sie Ihre Änderungen vorgenommen und eine Vorschau des Effekts angezeigt haben, sollten Sie die Seite durch Auswahl von **Einchecken** auf der Befehlsleiste einchecken.</span><span class="sxs-lookup"><span data-stu-id="b601f-130">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Check in** on the command bar.</span></span> 

<span data-ttu-id="b601f-131">Um Ihre Änderungen umgehend zu veröffentlichen, wählen Sie **Veröffentlichen** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-131">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="b601f-132">Die zuletzt eingecheckte Version der Seite, die Sie geändert haben, wird veröffentlicht und steht externen Benutzern zur Verfügung, die Ihre Website anzeigen.</span><span class="sxs-lookup"><span data-stu-id="b601f-132">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="b601f-133">Beispiel: Das Video auf der Startseite ändern</span><span class="sxs-lookup"><span data-stu-id="b601f-133">Example: Change the video on the home page</span></span>

<span data-ttu-id="b601f-134">Das folgende Beispiel zeigt, wie Sie die Startseite ändern, indem Sie das im Video-Player-Modul angezeigte Video ändern.</span><span class="sxs-lookup"><span data-stu-id="b601f-134">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="b601f-135">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-135">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="b601f-136">Wählen Sie im Navigationsbereich links **Seiten** aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-136">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="b601f-137">Suchen Sie die Startseite und wählen Sie sie aus, um sie im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b601f-137">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="b601f-138">Wählen Sie in der Befehlsleiste **Auschecken** aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-138">On the command bar, select **Check Out**.</span></span>
1. <span data-ttu-id="b601f-139">Wählen Sie in der Seitengliederung den **Haupt**-Slot aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-139">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="b601f-140">Erweitern Sie unter dem **Haupt**-Slot alle flüssigen Containermodule.</span><span class="sxs-lookup"><span data-stu-id="b601f-140">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="b601f-141">Suchen Sie das Video-Player-Modul und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-141">Find and select the video player module.</span></span>
1. <span data-ttu-id="b601f-142">Wählen Sie im Eigenschaftenbereich rechts die Eigenschaft **Video** aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-142">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="b601f-143">Die Anlagen-Auswahl wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b601f-143">The asset picker appears.</span></span>
1. <span data-ttu-id="b601f-144">Wählen Sie in der Anlagen-Auswahl eine verfügbare Videoanlage oder **Neue Anlage hochladen** aus, um eine neue Videoanlage hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="b601f-144">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="b601f-145">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="b601f-145">Select **OK**.</span></span>
1. <span data-ttu-id="b601f-146">Wählen Sie **Speichern** und dann **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-146">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="b601f-147">Geben Sie im Feld **Kommentare** **Video geändert** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-147">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="b601f-148">Wählen Sie **Vorschau** aus, um die aktualisierte Seite in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b601f-148">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="b601f-149">Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="b601f-149">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="b601f-150">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="b601f-150">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b601f-151">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b601f-151">Additional resources</span></span>

[<span data-ttu-id="b601f-152">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="b601f-152">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="b601f-153">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="b601f-153">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="b601f-154">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="b601f-154">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="b601f-155">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="b601f-155">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="b601f-156">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="b601f-156">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="b601f-157">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="b601f-157">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="b601f-158">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="b601f-158">Verify page content accessibility</span></span>](verify-accessibility.md)
