---
title: Dynamische E-Commerce-Seiten anhand von URL-Parametern erstellen
description: In diesem Thema wird erläutert, wie Sie eine E-Commerce-Seite in Microsoft Dynamics 365 Commerce einrichten, die basierend auf URL-Parametern dynamischen Inhalt bereitstellen kann.
author: StuHarg
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 8f59b80880e6947e1b45c110df0e78d4bdd57c5d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795810"
---
# <a name="create-dynamic-e-commerce-pages-based-on-url-parameters"></a><span data-ttu-id="cfd25-103">Dynamische E-Commerce-Seiten anhand von URL-Parametern erstellen</span><span class="sxs-lookup"><span data-stu-id="cfd25-103">Create dynamic e-commerce pages based on URL parameters</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cfd25-104">In diesem Thema wird erläutert, wie Sie eine E-Commerce-Seite in Microsoft Dynamics 365 Commerce einrichten, die basierend auf URL-Parametern dynamischen Inhalt bereitstellen kann.</span><span class="sxs-lookup"><span data-stu-id="cfd25-104">This topic describes how to set up a Microsoft Dynamics 365 Commerce e-commerce page that can serve dynamic content, based on URL parameters.</span></span>

<span data-ttu-id="cfd25-105">Eine E-Commerce-Seite kann so konfiguriert werden, dass sie unterschiedliche Inhalte basierend auf einem Segment im URL-Pfad bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="cfd25-105">An e-commerce page can be configured to serve different content, based on a segment in the URL path.</span></span> <span data-ttu-id="cfd25-106">Daher wird die Seite als dynamische Seite bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="cfd25-106">Therefore, the page is known as a dynamic page.</span></span> <span data-ttu-id="cfd25-107">Das Segment wird als Parameter zum Abrufen des Seiteninhalts verwendet.</span><span class="sxs-lookup"><span data-stu-id="cfd25-107">The segment is used as a parameter to retrieve the page content.</span></span> <span data-ttu-id="cfd25-108">So wird beispielsweise eine Seite namens **Blog\_Zuschauer** erstellt und der URL `https://fabrikam.com/blog` zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cfd25-108">For example, a page that is named **blog\_viewer** is created and associated with the URL `https://fabrikam.com/blog`.</span></span> <span data-ttu-id="cfd25-109">Diese Seite kann dann verwendet werden, um unterschiedliche Inhalte basierend auf dem letzten Segment im URL-Pfad anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="cfd25-109">This page can then be used to show different content, based on the last segment in the URL path.</span></span> <span data-ttu-id="cfd25-110">Zum Beispiel ist das letzte Segment in der URL `https://fabrikam.com/blog/article-1` **Artikel-1**.</span><span class="sxs-lookup"><span data-stu-id="cfd25-110">For example, the last segment in the URL `https://fabrikam.com/blog/article-1` is **article-1**.</span></span>

<span data-ttu-id="cfd25-111">Separate benutzerdefinierte Seiten, die die dynamische Seite überschreiben, können auch Segmenten im URL-Pfad zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="cfd25-111">Separate custom pages that override the dynamic page can also be associated with segments in the URL path.</span></span> <span data-ttu-id="cfd25-112">So wird beispielsweise eine Seite namens **Blog\_Zusammenfassung** erstellt und der URL `https://fabrikam.com/blog/about-this-blog` zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cfd25-112">For example, a page that is named **blog\_summary** is created and associated with the URL `https://fabrikam.com/blog/about-this-blog`.</span></span> <span data-ttu-id="cfd25-113">Wird diese URL angefordert, wird die Seite **Blog\_Zusammenfassung**, die dem Parameter **/über-diesen-Blog** zugeordnet ist, anstelle der Seite **Blog\_Zuschauer** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cfd25-113">When this URL is requested, the **blog\_summary** page that is associated with the **/about-this-blog** parameter is returned instead of the **blog\_viewer** page.</span></span>

> [!NOTE]
> <span data-ttu-id="cfd25-114">Die Funktionen zum Hosten, Abrufen und Anzeigen dynamischer Seiteninhalte werden mithilfe eines benutzerdefinierten Moduls implementiert.</span><span class="sxs-lookup"><span data-stu-id="cfd25-114">The functionality for hosting, retrieving, and showing dynamic page content is implemented by using a custom module.</span></span> <span data-ttu-id="cfd25-115">Weitere Informationen finden Sie unter [Onlinekanalerweiterbarkeit](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="cfd25-115">For more information, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

## <a name="set-up-a-dynamic-e-commerce-page"></a><span data-ttu-id="cfd25-116">Eine dynamische E-Commerce-Seite einrichten</span><span class="sxs-lookup"><span data-stu-id="cfd25-116">Set up a dynamic e-commerce page</span></span>

<span data-ttu-id="cfd25-117">Um eine dynamische E-Commerce-Seite einzurichten, müssen Sie die dynamische Seite sowie die Basis-URL erstellen und die Route zur dynamischen Seite konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cfd25-117">To set up a dynamic e-commerce page, you must create the dynamic page, create the base URL, and configure the route to the dynamic page.</span></span>

### <a name="create-the-page-that-will-serve-dynamic-content"></a><span data-ttu-id="cfd25-118">Die Seite, die dynamischen Inhalt bereitstellt, erstellen</span><span class="sxs-lookup"><span data-stu-id="cfd25-118">Create the page that will serve dynamic content</span></span>

<span data-ttu-id="cfd25-119">Führen Sie die folgenden Schritte aus, um eine Seite zu erstellen, die dynamischen Inhalt bereitstellt [Eine neue Website-Seite hinzufügen](add-new-page.md).</span><span class="sxs-lookup"><span data-stu-id="cfd25-119">To create a page that will serve dynamic content, follow the steps in [Add a new site page](add-new-page.md).</span></span> <span data-ttu-id="cfd25-120">Für die von Ihnen erstellte Seite muss ein Modul implementiert werden, das das letzte Segment im URL-Pfad verwendet, um Inhalte aus einer externen Datenquelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="cfd25-120">The page that you create will require implementation of a module that uses the last segment in the URL path to retrieve content from an external data source.</span></span> <span data-ttu-id="cfd25-121">Weitere Informationen zur Entwicklung benutzerdefinierter Module finden Sie unter [Onlinekanalerweiterbarkeit](e-commerce-extensibility/overview.md).</span><span class="sxs-lookup"><span data-stu-id="cfd25-121">For more information about custom module development, see [Online channel extensibility](e-commerce-extensibility/overview.md).</span></span>

### <a name="create-the-base-url-for-the-dynamic-page"></a><span data-ttu-id="cfd25-122">Die Basis-URL für die dynamische Seite erstellen</span><span class="sxs-lookup"><span data-stu-id="cfd25-122">Create the base URL for the dynamic page</span></span>

<span data-ttu-id="cfd25-123">Führen Sie die folgenden Schritte aus, um die Basis-URL für die dynamische Seite im Commerce-Website-Generator zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="cfd25-123">To create the base URL for the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cfd25-124">Rufen Sie **URLs** auf, und wählen Sie **Neu \> Neue URL** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-124">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="cfd25-125">Wählen Sie im Dialogfeld **Neue URL erstellen** die Option **Interne Seite** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-125">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="cfd25-126">Egen Sie unter **URL-Pfad** den Pfad ein, der als Stamm für die dynamische Seite dient (in diesem Beispiel: **/Blog**).</span><span class="sxs-lookup"><span data-stu-id="cfd25-126">Under **URL path**, enter the path that will serve as the root for the dynamic page (in this example, **/blog**).</span></span> <span data-ttu-id="cfd25-127">Wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-127">Then select **Next**.</span></span>
1. <span data-ttu-id="cfd25-128">Wählen Sie im Dialogfeld **Eine Seite auswählen** die Seite aus, die Sie zuvor als dynamische Seite erstellt haben, und wählen Sie dann **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-128">In the **Select a page** dialog box, select the page that you created to serve as the dynamic page, and then select **Save**.</span></span>
1. <span data-ttu-id="cfd25-129">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-129">Select **Publish**.</span></span>

### <a name="configure-the-route-to-the-dynamic-page"></a><span data-ttu-id="cfd25-130">Die Route zur dynamischen Seite konfigurieren</span><span class="sxs-lookup"><span data-stu-id="cfd25-130">Configure the route to the dynamic page</span></span>

<span data-ttu-id="cfd25-131">Führen Sie die folgenden Schritte aus, um die Route zu der dynamischen Seite im Commerce-Website-Generator zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cfd25-131">To configure the route to the dynamic page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cfd25-132">Gehen Sie zu **Seiteneinstellungen \> Erweiterungen**.</span><span class="sxs-lookup"><span data-stu-id="cfd25-132">Go to **Site Settings \> Extensions**.</span></span>
1. <span data-ttu-id="cfd25-133">Wählen Sie unter **Parametrisierte URL-Pfade** die Option **Hinzufügen** aus. Geben Sie dann den URL-Pfad ein, den Sie beim Erstellen der URL eingegeben haben (in diesem Beispiel: **/Blog**).</span><span class="sxs-lookup"><span data-stu-id="cfd25-133">Under **Parameterized URL paths**, select **Add**, and then enter the URL path that you entered when you created the URL (in this example, **/blog**).</span></span>
1. <span data-ttu-id="cfd25-134">Wählen Sie **Speichern und veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-134">Select **Save and publish**.</span></span>

<span data-ttu-id="cfd25-135">Sobald die Route konfiguriert wurde, geben alle Anfragen an den parametrisierten URL-Pfad die Seite zurück, die dieser URL zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cfd25-135">After the route is configured, all requests to the parameterized URL path will return the page that is associated with that URL.</span></span> <span data-ttu-id="cfd25-136">Wenn Anfragen ein zusätzliches Segment enthalten, wird die zugehörige Seite zurückgegeben und der Seiteninhalt mithilfe des Segments als Parameter abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cfd25-136">If any requests contain an additional segment, the associated page will be returned, and the page content will be retrieved by using the segment as a parameter.</span></span> <span data-ttu-id="cfd25-137">Beispielsweise gibt `https://fabrikam.com/blog/article-1` die Seite **Blog\_Zusammenfassung** zurück, und der Seiteninhalt wird mithilfe des **/Artikel-1**-Parameters abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cfd25-137">For example, `https://fabrikam.com/blog/article-1` will return the **blog\_summary** page, and the page content will be retrieved by using the **/article-1** parameter.</span></span>

## <a name="override-a-parameterized-url-with-a-custom-page"></a><span data-ttu-id="cfd25-138">Eine parametrisierte URL mit einer benutzerdefinierten Seite überschreiben</span><span class="sxs-lookup"><span data-stu-id="cfd25-138">Override a parameterized URL with a custom page</span></span>

<span data-ttu-id="cfd25-139">Führen Sie die folgenden Schritte aus, um eine parametrisierte URL mit einer benutzerdefinierten Seite im Commerce-Website-Generator zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="cfd25-139">To override a parameterized URL with a custom page in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="cfd25-140">Rufen Sie **URLs** auf, und wählen Sie **Neu \> Neue URL** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-140">Go to **URLs**, and select **New \> New URL**.</span></span>
1. <span data-ttu-id="cfd25-141">Wählen Sie im Dialogfeld **Neue URL erstellen** die Option **Interne Seite** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-141">In the **Create new URL** dialog box, select **Internal page**.</span></span> <span data-ttu-id="cfd25-142">Geben Sie unter **URL-Pfad** den Pfad ein, der das zu überschreibende Segment enthält (in diesem Beispiel: **/Blog/über-diesen-Blog**).</span><span class="sxs-lookup"><span data-stu-id="cfd25-142">Under **URL path**, enter the path that includes the segment to override (in this example, **/blog/about-this-blog**).</span></span> <span data-ttu-id="cfd25-143">Wählen Sie dann **Weiter** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-143">Then select **Next**.</span></span>
1. <span data-ttu-id="cfd25-144">Wählen Sie im Dialogfeld **Eine Seite auswählen** die benutzerdefinierte Seite und anschließend **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-144">In the **Select a page** dialog box, select the custom page, and then select **Save**.</span></span>
1. <span data-ttu-id="cfd25-145">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-145">Select **Publish**.</span></span>
1. <span data-ttu-id="cfd25-146">Wenn die benutzerdefinierte Seite noch nicht veröffentlicht wurde, rufen Sie **Seiten** auf, wählen Sie die benutzerdefinierte Seite und anschließend **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="cfd25-146">If the custom page hasn't yet been published, go to **Pages**, select the custom page, and then select **Publish**.</span></span>

<span data-ttu-id="cfd25-147">Nachdem die benutzerdefinierte Seite veröffentlicht wurde, wird sie anstelle der dynamischen Seite mit parametrisiertem Inhalt bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cfd25-147">After the custom page is published, it will be served instead of the dynamic page that has parameterized content.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cfd25-148">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cfd25-148">Additional resources</span></span>

[<span data-ttu-id="cfd25-149">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="cfd25-149">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="cfd25-150">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="cfd25-150">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="cfd25-151">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="cfd25-151">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="cfd25-152">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="cfd25-152">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="cfd25-153">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="cfd25-153">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="cfd25-154">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="cfd25-154">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="cfd25-155">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="cfd25-155">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="cfd25-156">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="cfd25-156">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="cfd25-157">Onlinekanalerweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="cfd25-157">Online channel extensibility</span></span>](e-commerce-extensibility/overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
