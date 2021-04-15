---
title: Bestehende Seite einer Website ändern
description: In diesem Thema wird beschrieben, wie Sie eine vorhandene Websiteseite in Microsoft Dynamics 365 Commerce ändern.
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
ms.openlocfilehash: b633965e45c16cb4e5991fab67783b867223f6ec
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803728"
---
# <a name="modify-an-existing-site-page"></a><span data-ttu-id="e9005-103">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="e9005-103">Modify an existing site page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e9005-104">In diesem Thema wird beschrieben, wie Sie eine vorhandene Websiteseite in Microsoft Dynamics 365 Commerce ändern.</span><span class="sxs-lookup"><span data-stu-id="e9005-104">This topic describes how to modify an existing site page in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="e9005-105">Wenn Sie eine Seite ändern müssen, müssen Sie sie zunächst im Seiteneditor öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9005-105">When you must modify a page, the first step is to open it in the page editor.</span></span> <span data-ttu-id="e9005-106">Gehen Sie zu der Site, die Ihre Seite enthält, und suchen Sie dann in der Liste der Seiten die gewünschte Seite.</span><span class="sxs-lookup"><span data-stu-id="e9005-106">Go to the site that contains your page, and then, in the list of pages, find the page that you want.</span></span> <span data-ttu-id="e9005-107">Wenn Sie die Seite nicht finden können, können Sie die umfangreiche Suchfunktion des Erstellungstools verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9005-107">If you can't find the page, you can use the authoring tool's rich search functionality.</span></span> <span data-ttu-id="e9005-108">Geben Sie entweder den genauen Seitennamen oder die ersten Buchstaben und dann ein Sternchen ein (\*).</span><span class="sxs-lookup"><span data-stu-id="e9005-108">Either type the exact page name, or type the first few letters of it and then an asterisk (\*).</span></span> <span data-ttu-id="e9005-109">Eine gefilterte Liste der Seiten wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9005-109">A filtered list of pages appears.</span></span> <span data-ttu-id="e9005-110">Sie können diese Liste verwenden, um die gewünschte Seite zu finden.</span><span class="sxs-lookup"><span data-stu-id="e9005-110">You can use this list to find the page that you want.</span></span> <span data-ttu-id="e9005-111">Nachdem Sie die richtige Seite gefunden haben, wählen Sie den Seitennamen aus, um die Seite im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9005-111">After you find the correct page, select the page name to open the page in the page editor.</span></span>

> [!TIP]
> <span data-ttu-id="e9005-112">Wenn Ihre Seite im Seiteninspektor angezeigt wird, können Sie **Bearbeiten** auswählen und sie auschecken, bevor Sie sie im Seiteneditor öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9005-112">If your page is visible in the page inspector, you can select **Edit** and check the page out before you open it in the page editor.</span></span> <span data-ttu-id="e9005-113">Auf diese Weise können Sie mehrere Seiten gleichzeitig auschecken.</span><span class="sxs-lookup"><span data-stu-id="e9005-113">In this way, you can check out multiple pages at the same time.</span></span>

<span data-ttu-id="e9005-114">Nachdem die Seite im Seiteneditor geöffnet wurde, müssen Sie sicherstellen, dass sie für Sie ausgecheckt ist.</span><span class="sxs-lookup"><span data-stu-id="e9005-114">After the page is open in the page editor, you must make sure that it's checked out to you.</span></span> <span data-ttu-id="e9005-115">Die Befehlsleiste im Erstellungstools ist dynamisch, kontextbezogen und statusabhängig.</span><span class="sxs-lookup"><span data-stu-id="e9005-115">The command bar in the authoring tool is dynamic, context-sensitive, and state-sensitive.</span></span> <span data-ttu-id="e9005-116">Daher werden nur die Aktionen angezeigt, die Sie derzeit auf der Seite ausführen können.</span><span class="sxs-lookup"><span data-stu-id="e9005-116">Therefore, it shows only the actions that you can currently perform on the page.</span></span> <span data-ttu-id="e9005-117">Wenn die Seite beispielsweise nicht für Sie ausgecheckt wurde, werden die Schalflächen **Speichern** und **Bearbeiten beenden** nicht in der Befehlsleiste angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9005-117">For example, if the page isn't checked out to you, the **Save** and **Finish editing** buttons don't appear on the command bar.</span></span> <span data-ttu-id="e9005-118">Der Status der Seite wird auch auf der rechten Seite des Fensters angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9005-118">The state of the page is also shown on the right side of the window.</span></span>

<span data-ttu-id="e9005-119">Wenn die Seite noch nicht für Sie ausgecheckt wurde, wählen Sie **Bearbeiten** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-119">If the page isn't already checked out to you, select **Edit** on the command bar.</span></span> <span data-ttu-id="e9005-120">Die Befehlsleiste ändert sich, um den neuen Status der Seite widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="e9005-120">The command bar changes to reflect the new state of the page.</span></span> <span data-ttu-id="e9005-121">Sie erhalten auch eine Benachrichtigung, die besagt, dass die Seite für Sie ausgecheckt wurde.</span><span class="sxs-lookup"><span data-stu-id="e9005-121">You also receive a notification that states that the page was checked out to you.</span></span>

<span data-ttu-id="e9005-122">Der nächste Schritt besteht darin, Ihre tatsächlichen Änderungen vorzunehmen.</span><span class="sxs-lookup"><span data-stu-id="e9005-122">The next step is to make your actual changes.</span></span> <span data-ttu-id="e9005-123">Häufig verwenden Sie die Seitengliederungsstruktur auf der linken Seite, um das zu ändernde Modul zu suchen und auszuwählen, und nehmen dann im Eigenschaftsfenster auf der rechten Seite Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="e9005-123">Often, you will use the page outline tree on the left to find and select the module that you want to change, and then make changes in the properties pane on the right.</span></span> 

<span data-ttu-id="e9005-124">Ihre Änderung kann jedoch manchmal das Hinzufügen oder Entfernen von Modellen oder Fragmenten umfassen.</span><span class="sxs-lookup"><span data-stu-id="e9005-124">However, your change might sometimes involve adding or removing models or fragments.</span></span> <span data-ttu-id="e9005-125">Um ein Fragment oder Modul hinzuzufügen, suchen Sie in der Seitenstruktur den Slot, dem Sie das Modul oder Fragment hinzufügen möchten, und klicken Sie dann auf die Schaltfläche mit den Auslassungspunkten (**...**) für diesen Slot.</span><span class="sxs-lookup"><span data-stu-id="e9005-125">To add a fragment or module, use the page outline tree to find the slot that you want to add the module or fragment to, and then select the ellipsis button (**...**) for that slot.</span></span> <span data-ttu-id="e9005-126">Ein Menü mit Befehlen zum Hinzufügen eines Moduls oder Fragments wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9005-126">A menu appears that includes commands for adding a module or fragment.</span></span> <span data-ttu-id="e9005-127">Um ein Modul oder Fragment zu entfernen, suchen Sie es und wählen Sie es in der Seitenstruktur aus, klicken Sie auf die Schaltfläche mit den Auslassungspunkten und wählen Sie dann den Befehl zum Löschen des Moduls oder Fragments aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-127">To remove a module or fragment, find and select it in the page outline tree, select the ellipsis button, and then select the command to delete the module or fragment.</span></span>

> [!TIP]
> <span data-ttu-id="e9005-128">Sie können auch die Eigenschaften für jedes Modul anzeigen und bearbeiten, das in der Visual Page Builder-Vorschau angezeigt wird, indem Sie es direkt auswählen.</span><span class="sxs-lookup"><span data-stu-id="e9005-128">You can also view and edit the properties for any module that is visible in the visual page builder preview by selecting it directly.</span></span>

<span data-ttu-id="e9005-129">Nachdem Sie Ihre Änderungen vorgenommen und eine Vorschau des Effekts angezeigt haben, sollten Sie die Seite durch Auswahl von **Bearbeiten beenden** auf der Befehlsleiste einchecken.</span><span class="sxs-lookup"><span data-stu-id="e9005-129">After you've finished making your changes and previewing their effect, you should check in the page by selecting **Finish editing** on the command bar.</span></span> 

<span data-ttu-id="e9005-130">Um Ihre Änderungen umgehend zu veröffentlichen, wählen Sie **Veröffentlichen** in der Befehlsleiste aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-130">To publish your changes immediately, select **Publish** on the command bar.</span></span> <span data-ttu-id="e9005-131">Die zuletzt eingecheckte Version der Seite, die Sie geändert haben, wird veröffentlicht und steht externen Benutzern zur Verfügung, die Ihre Website anzeigen.</span><span class="sxs-lookup"><span data-stu-id="e9005-131">The latest checked-in version of the page that you modified is published and becomes available to external users who view your site.</span></span> 

## <a name="example-change-the-video-on-the-home-page"></a><span data-ttu-id="e9005-132">Beispiel: Das Video auf der Startseite ändern</span><span class="sxs-lookup"><span data-stu-id="e9005-132">Example: Change the video on the home page</span></span>

<span data-ttu-id="e9005-133">Das folgende Beispiel zeigt, wie Sie die Startseite ändern, indem Sie das im Video-Player-Modul angezeigte Video ändern.</span><span class="sxs-lookup"><span data-stu-id="e9005-133">The following example shows how to modify the home page by changing the video that appears in the video player module.</span></span>

1. <span data-ttu-id="e9005-134">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-134">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="e9005-135">Wählen Sie im Navigationsbereich links **Seiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-135">In the navigation pane on the left, select **Pages**.</span></span>
1. <span data-ttu-id="e9005-136">Suchen Sie die Startseite und wählen Sie sie aus, um sie im Seiteneditor zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9005-136">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="e9005-137">Wählen Sie in der Befehlsleiste **Bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-137">On the command bar, select **Edit**.</span></span>
1. <span data-ttu-id="e9005-138">Wählen Sie in der Seitengliederung den **Haupt**-Slot aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-138">In the page outline, select the **Main** slot.</span></span>
1. <span data-ttu-id="e9005-139">Erweitern Sie unter dem **Haupt**-Slot alle flüssigen Containermodule.</span><span class="sxs-lookup"><span data-stu-id="e9005-139">Under the **Main** slot, expand all the fluid container modules.</span></span>
1. <span data-ttu-id="e9005-140">Suchen Sie das Video-Player-Modul und wählen Sie es aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-140">Find and select the video player module.</span></span>
1. <span data-ttu-id="e9005-141">Wählen Sie im Eigenschaftenbereich rechts die Eigenschaft **Video** aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-141">In the properties pane on the right, select the **video** property.</span></span> <span data-ttu-id="e9005-142">Die Anlagen-Auswahl wird angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e9005-142">The asset picker appears.</span></span>
1. <span data-ttu-id="e9005-143">Wählen Sie in der Anlagen-Auswahl eine verfügbare Videoanlage oder **Neue Anlage hochladen** aus, um eine neue Videoanlage hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="e9005-143">In the asset picker, select an available video asset, or select **Upload new asset** to upload a new video asset.</span></span>
1. <span data-ttu-id="e9005-144">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="e9005-144">Select **OK**.</span></span>
1. <span data-ttu-id="e9005-145">Wählen Sie **Speichern** und dann **Bearbeiten beenden** aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-145">Select **Save**, and then select **Finish editing**.</span></span>
1. <span data-ttu-id="e9005-146">Geben Sie im Feld **Kommentare** **Video geändert** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-146">In the **Comments** field, enter **Changed the video**, and then select **OK**.</span></span>
1. <span data-ttu-id="e9005-147">Wählen Sie **Vorschau** aus, um die aktualisierte Seite in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="e9005-147">Select **Preview** to preview the updated page.</span></span> <span data-ttu-id="e9005-148">Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="e9005-148">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="e9005-149">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="e9005-149">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e9005-150">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e9005-150">Additional resources</span></span>

[<span data-ttu-id="e9005-151">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="e9005-151">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="e9005-152">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="e9005-152">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="e9005-153">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="e9005-153">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="e9005-154">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="e9005-154">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="e9005-155">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="e9005-155">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="e9005-156">Kategoriezielseite erweitern</span><span class="sxs-lookup"><span data-stu-id="e9005-156">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="e9005-157">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="e9005-157">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="e9005-158">Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen</span><span class="sxs-lookup"><span data-stu-id="e9005-158">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
