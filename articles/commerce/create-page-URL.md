---
title: Erstellen einer Seiten-URL
description: In diesem Thema werden grundlegende Konzepte und Verfahren zum Erstellen einer Seiten-URL auf Ihrer Site behandelt.
author: bicyclingfool
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
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ab7325dd4060392ed43e59c1ad48069d294d81c0
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697547"
---
# <a name="create-a-page-url"></a><span data-ttu-id="afd2d-103">Erstellen einer Seiten-URL</span><span class="sxs-lookup"><span data-stu-id="afd2d-103">Create a page URL</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="afd2d-104">In diesem Thema werden grundlegende Konzepte und Verfahren zum Erstellen einer Seiten-URL auf Ihrer Site behandelt.</span><span class="sxs-lookup"><span data-stu-id="afd2d-104">This topic covers the basic concepts and procedures for creating a page URL on your site.</span></span>

## <a name="overview"></a><span data-ttu-id="afd2d-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="afd2d-105">Overview</span></span>

<span data-ttu-id="afd2d-106">Der vollständige oder absolute URL die auf eine Seite auf Ihrer Site verweist, besteht aus eindeutigen Teilen.</span><span class="sxs-lookup"><span data-stu-id="afd2d-106">The full, or absolute, URL that points to a page on your site consists of distinct parts.</span></span> <span data-ttu-id="afd2d-107">Zum Beispiel verfügt die URL `https://www.contoso.com/en-us/contactus` über folgende Bereiche:</span><span class="sxs-lookup"><span data-stu-id="afd2d-107">For example, the URL `https://www.contoso.com/en-us/contactus` has the following parts:</span></span>

- <span data-ttu-id="afd2d-108">`https://www.contoso.com` – Das HTTP-Protokoll und die Domäne des Standorts.</span><span class="sxs-lookup"><span data-stu-id="afd2d-108">`https://www.contoso.com` – The HTTP protocol and the site's domain.</span></span>
- <span data-ttu-id="afd2d-109">`/en-us` – Der Sprachenpfad der Site.</span><span class="sxs-lookup"><span data-stu-id="afd2d-109">`/en-us` – The site's language path.</span></span>
- <span data-ttu-id="afd2d-110">`/contactus` – Die relative URL für die Seite **Kontaktieren Sie uns**.</span><span class="sxs-lookup"><span data-stu-id="afd2d-110">`/contactus` – The relative URL for the **Contact Us** page.</span></span> <span data-ttu-id="afd2d-111">Eine relative URL ist auch als ein URL *Titel* bekannt.</span><span class="sxs-lookup"><span data-stu-id="afd2d-111">A relative URL is also known as a URL *slug*.</span></span>

<span data-ttu-id="afd2d-112">Sie richten die Domäne Ihrer Site und den optionalen Sprachenpfad ein, wenn Sie die Site einrichten.</span><span class="sxs-lookup"><span data-stu-id="afd2d-112">You establish your site's domain and optional language path when you set up the site.</span></span> <span data-ttu-id="afd2d-113">Sie können mehrere Domänen und Sprachenpfade Ihrer Site über die Onlineshopseite in den Einstellungen der Site hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="afd2d-113">You can add more domains and language paths to your site through the online stores page in the site's settings.</span></span>

<span data-ttu-id="afd2d-114">Der URL-Titel für eine Seite ist als eigenständige Entität in der Siteerstellungsumgebung vorhanden.</span><span class="sxs-lookup"><span data-stu-id="afd2d-114">The URL slug for a page exists as a standalone entity in the site authoring environment.</span></span> <span data-ttu-id="afd2d-115">Eine Seiten-URL besteht aus zwei Teilen: ein Name, der den URL-Titel darstellt und eine Verknüpfung zu einer Seite, entweder zu Ihrer Site oder einer externen Site.</span><span class="sxs-lookup"><span data-stu-id="afd2d-115">A page URL consists of two parts: a name that represents the URL slug, and a pointer to a page on either your site or an external site.</span></span> <span data-ttu-id="afd2d-116">Eine Seiten-URL kann auch so konfiguriert werden, dass sie als Umleitung zu einer anderen Seite entweder auf Ihre Site oder eine externe Site zu dienen.</span><span class="sxs-lookup"><span data-stu-id="afd2d-116">A page URL can also be configured to act as a redirect to another page on either your site or an external site.</span></span>

## <a name="create-a-page-url"></a><span data-ttu-id="afd2d-117">Erstellen einer Seiten-URL</span><span class="sxs-lookup"><span data-stu-id="afd2d-117">Create a page URL</span></span>

<span data-ttu-id="afd2d-118">Es gibt zwei Möglichkeiten, Seiten-URLs zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="afd2d-118">There are two ways to create page URLs:</span></span>

- <span data-ttu-id="afd2d-119">Automatisch wenn Sie eine Seite erstellen</span><span class="sxs-lookup"><span data-stu-id="afd2d-119">Automatically, when you create a page</span></span>
- <span data-ttu-id="afd2d-120">Manuell von den Seiten-**URLs**</span><span class="sxs-lookup"><span data-stu-id="afd2d-120">Manually, from the **URLs** page</span></span>

### <a name="create-a-page-url-when-you-create-a-page"></a><span data-ttu-id="afd2d-121">Hier können Sie eine Seiten-URL erstellen, wenn Sie eine Seite erstellen</span><span class="sxs-lookup"><span data-stu-id="afd2d-121">Create a page URL when you create a page</span></span>

<span data-ttu-id="afd2d-122">Wenn Sie einen Namen im Feld **URL** angeben, wenn Sie eine neue Seite erstellen, wird eine Seiten-URL, die auf diese Seite verweist, automatisch auf den Seiten **URLs** erstellt.</span><span class="sxs-lookup"><span data-stu-id="afd2d-122">If you provide a name in the **URL** field when you create a new page, a page URL that points to that page is automatically created on the **URLs** page.</span></span> <span data-ttu-id="afd2d-123">Nachdem Sie die URL und die Seite veröffentlicht haben, auf die verwiesen wird, können Site-Benutzer (Ihre Debitoren) auf die Seite zugreifen, die mit der URL verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="afd2d-123">After you publish the URL and the page that it points to, site users (your customers) can access the page that is associated with the URL.</span></span>

> [!NOTE]
> <span data-ttu-id="afd2d-124">Wenn Sie eine URL veröffentlichen, ohne die Seite zu veröffentlichen, auf die verwiesen wird, erhalten Sitebenutzer einen Fehlercode 404, wenn Sie versuchen, die Seite zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="afd2d-124">If you publish a URL without publishing the page that it points to, site users receive a 404 error when they try to access the page.</span></span> <span data-ttu-id="afd2d-125">Wenn Sie eine Seite veröffentlichen, ohne die URL zu veröffentlichen, die darauf verweist, kann nicht auf die Seite nicht mithilfe der URL zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="afd2d-125">If you publish a page without publishing the URL that points to it, the page can't be accessed by using a URL.</span></span>

### <a name="manually-create-a-page-url"></a><span data-ttu-id="afd2d-126">Manuell eine Seiten-URL erstellen</span><span class="sxs-lookup"><span data-stu-id="afd2d-126">Manually create a page URL</span></span>

<span data-ttu-id="afd2d-127">Wenn Sie neue Seiten erstellen, müssen Sie keine Seiten-URL definieren.</span><span class="sxs-lookup"><span data-stu-id="afd2d-127">When you create new pages, you aren't required to specify a page URL.</span></span> <span data-ttu-id="afd2d-128">Wenn Sie das URL Feld leer lassen, wird die Seite in einem nicht verknüpften Status erstellt.</span><span class="sxs-lookup"><span data-stu-id="afd2d-128">If you leave the URL field blank, the page is created in an unlinked state.</span></span> <span data-ttu-id="afd2d-129">In diesem Fall sind Debitoren nicht in der Lage, auf die Seite zuzugreifen, selbst wenn sie veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="afd2d-129">In this case, customers won't be able to access the page, even if it's published.</span></span> <span data-ttu-id="afd2d-130">Um die Seite verfügbar zu machen, müssen Sie die URL manuell erstellen und diese mit der Seite verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="afd2d-130">To make the page accessible, you must manually create the URL and link it to the page.</span></span>

<span data-ttu-id="afd2d-131">Um die Seiten-URL manuell für eine Seite zu erstellen, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="afd2d-131">To manually create the page URL for a page, follow these steps.</span></span>

1. <span data-ttu-id="afd2d-132">Wählen Sie auf der Seite **URL** die Option **Neu** aus.</span><span class="sxs-lookup"><span data-stu-id="afd2d-132">On the **URLs** page, select **New**.</span></span>
1. <span data-ttu-id="afd2d-133">Wählen Sie die Siteseite, die mit der URL verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="afd2d-133">Select the site page to associate with the URL.</span></span>
1. <span data-ttu-id="afd2d-134">Geben Sie den URL-Titel ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="afd2d-134">Enter the URL slug, and then select **OK**.</span></span>

<span data-ttu-id="afd2d-135">An diesem Punkt ist die URL in einem Entwurfzustand.</span><span class="sxs-lookup"><span data-stu-id="afd2d-135">At this point, the URL is in a draft state.</span></span> <span data-ttu-id="afd2d-136">Sie muss veröffentlicht werden, bevor der Sitebenutzer auf die verknüpfte Seite zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="afd2d-136">It must be published before site users can access the associated page.</span></span>

## <a name="update-a-page-url"></a><span data-ttu-id="afd2d-137">Seiten-URL aktualisieren</span><span class="sxs-lookup"><span data-stu-id="afd2d-137">Update a page URL</span></span>

<span data-ttu-id="afd2d-138">Um die Zielseite einer Seiten-URL zu aktualisieren, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="afd2d-138">To update the target page of a page URL, follow these steps.</span></span>

1. <span data-ttu-id="afd2d-139">Wählen Sie auf der Seite **URLs** die URL aus, um sie zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="afd2d-139">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="afd2d-140">Im Eigenschaftenbereich auf der rechten Seite klicken Sie auf die Ellipsen.Schaltfläche (**…**) neben dem Zielseitenfeld.</span><span class="sxs-lookup"><span data-stu-id="afd2d-140">In the property pane on the right, select the ellipsis button (**...**) next to the target page field.</span></span>
1. <span data-ttu-id="afd2d-141">Wählen Sie im Dialogfeld eine andere Seite wählen dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="afd2d-141">In the dialog box, select a different page, and then select **OK**.</span></span>
1. <span data-ttu-id="afd2d-142">URL speichern und veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="afd2d-142">Save and publish the URL.</span></span>

## <a name="redirect-a-page-url"></a><span data-ttu-id="afd2d-143">Seiten-URL umleiten</span><span class="sxs-lookup"><span data-stu-id="afd2d-143">Redirect a page URL</span></span>

<span data-ttu-id="afd2d-144">Manchmal möchten Sie, dass Ihre Debitoren eine andere Seite angezeigt erhalten, wenn sie eine bestimmte URL anfordern.</span><span class="sxs-lookup"><span data-stu-id="afd2d-144">Sometimes, you might want your customers to view a different page when they request a specific URL.</span></span> <span data-ttu-id="afd2d-145">In diesen Fällen ist der beste und einfachste Ansatz häufig, die Seite zu ändern, auf die die Seiten-URL verweist.</span><span class="sxs-lookup"><span data-stu-id="afd2d-145">In these cases, the best and easiest approach is often to change the page that the page URL points to.</span></span> <span data-ttu-id="afd2d-146">Aber möglicherweise haben Sie bereichtigte Gründe, HTTP 301 oder 3023 zu verwenden, um die Anfrage für eine URL auf eine andere URL weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="afd2d-146">However, you might have legitimate reasons for using HTTP 301 or 3023 redirects to redirect requests for a URL to a different URL.</span></span>

<span data-ttu-id="afd2d-147">Um eine URL zu einer anderen URL weiterzuleiten, folgen Sie diesen Schritten.</span><span class="sxs-lookup"><span data-stu-id="afd2d-147">To redirect a URL to a different URL, follow these steps.</span></span>

1. <span data-ttu-id="afd2d-148">Wählen Sie auf der Seite **URLs** die URL aus, um sie zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="afd2d-148">On the **URLs** page, select the URL to update.</span></span>
1. <span data-ttu-id="afd2d-149">Wählen Sie im Eigenschaftenbereich rechts die Eigenschaft **Umleitung** aus.</span><span class="sxs-lookup"><span data-stu-id="afd2d-149">In the property pane on the right, select **Redirect**.</span></span>
1. <span data-ttu-id="afd2d-150">Wählen Sie ein Ziel für die Umleitung aus</span><span class="sxs-lookup"><span data-stu-id="afd2d-150">Select a destination for the redirect:</span></span>

    - <span data-ttu-id="afd2d-151">Um auf eine andere Seite auf Ihrer Site zu verweisen, wählen Sie **Interne URL**, wählen die Ellipsen-Schaltfläche (**...**) und wählen Sie anschließend die URL für die Umleitung.</span><span class="sxs-lookup"><span data-stu-id="afd2d-151">To point to another page on your site, select **Internal URL**, select the ellipsis button (**...**), and then select the URL to redirect to.</span></span>
    - <span data-ttu-id="afd2d-152">Um auf eine Seite auf einer externen Site zu verweisen, wählen Sie **Externe URL** und geben Sie dann die vollständige URL für diese Seite ein.</span><span class="sxs-lookup"><span data-stu-id="afd2d-152">To point to a page on an external site, select **External URL**, and then enter the full URL for that page.</span></span> <span data-ttu-id="afd2d-153">Achten Sie darauf, dass das Protokoll miteinbezogen wird.</span><span class="sxs-lookup"><span data-stu-id="afd2d-153">Be sure to include the protocol.</span></span> <span data-ttu-id="afd2d-154">Geben Sie beispielsweise `https://domain.com/new/page` ein.</span><span class="sxs-lookup"><span data-stu-id="afd2d-154">For example, enter `https://domain.com/new/page`.</span></span> <span data-ttu-id="afd2d-155">Wenn die URL bereits auf eine interne URL umleitet, müssen Sie **Auswahl löschen** auswählen, bevor Sie eine externe URL eingeben können.</span><span class="sxs-lookup"><span data-stu-id="afd2d-155">If the URL already redirects to an internal URL, you must select **Clear selection** before you can enter an external URL.</span></span>

1. <span data-ttu-id="afd2d-156">Wählen Sie einen Umleitungstyp aus.</span><span class="sxs-lookup"><span data-stu-id="afd2d-156">Select a redirect type:</span></span>

    - <span data-ttu-id="afd2d-157">**Permanente Umleitung (301)** – Wählen Sie diese Option aus, wenn Sie wissen, dass Ihr Inhalt dauerhaft verschoben wird und nicht zur vorherigen URL zurückkommt.</span><span class="sxs-lookup"><span data-stu-id="afd2d-157">**Permanent redirect (301)** – Select this option when you know that your content is moving permanently and won't revert to its previous URL.</span></span> <span data-ttu-id="afd2d-158">Suchmodule weisen den Suchmaschinen-Optimierungs (SEO)- Wert der umleitenden URL zu der URL zu, die umgeleitet wird und aktualisiert den Datensatz, um die neue URL anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="afd2d-158">Search engines will assign the search engine optimization (SEO) value of the redirecting URL to the URL that is being redirected to and update their record to show the new URL.</span></span> 
    - <span data-ttu-id="afd2d-159">**Temporäre Umleitung (302)** – Wählen Sie diese Option aus, um den Verkehr umzuleiten, ohne die Suchmodule zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="afd2d-159">**Temporary redirect (302)** – Select this option to redirect traffic without updating search engines.</span></span> <span data-ttu-id="afd2d-160">Dieser Ansatz wird normalerweise verwendet, wenn der Inhalt bald zur vorherigen URL zurückkehrt.</span><span class="sxs-lookup"><span data-stu-id="afd2d-160">This approach is typically used if the content will soon revert to its previous URL.</span></span>

1. <span data-ttu-id="afd2d-161">Wenn Sie bereit sind, die Umleitung zu implementieren, speichern und veröffentlichen Sie die URL.</span><span class="sxs-lookup"><span data-stu-id="afd2d-161">When you're ready to implement the redirect, save and publish the URL.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="afd2d-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="afd2d-162">Additional resources</span></span>

[<span data-ttu-id="afd2d-163">Anpassen der Sitenavigation</span><span class="sxs-lookup"><span data-stu-id="afd2d-163">Customize site navigation</span></span>](customize-site-navigation.md)

[<span data-ttu-id="afd2d-164">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="afd2d-164">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="afd2d-165">Konfigurieren Ihres Domänennamens</span><span class="sxs-lookup"><span data-stu-id="afd2d-165">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="afd2d-166">Hinzufügen von Sprachen zu Ihrer Website</span><span class="sxs-lookup"><span data-stu-id="afd2d-166">Add languages to your site</span></span>](add-languages-to-site.md)
