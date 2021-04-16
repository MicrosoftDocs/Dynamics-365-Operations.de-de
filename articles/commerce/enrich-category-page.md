---
title: Füllen einer Kategorie-Landingpage
description: In diesem Thema wird die Anreicherung der Kategorieseiten in Dynamics 365 Commerce abgedeckt.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5e18439fc0e91619cade33b83b87be0d5c4d1040
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799010"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="d0c10-103">Kategoriezielseite erweitern</span><span class="sxs-lookup"><span data-stu-id="d0c10-103">Enrich a category landing page</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d0c10-104">In diesem Thema wird die Anreicherung der Kategorieseiten in Dynamics 365 Commerce abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="d0c10-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="d0c10-105">Handel enthält eine Standardkategorieangebotsseite, die verwendet wird, wenn Kategoriedaten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d0c10-105">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="d0c10-106">Eine obligatorische Standardkategorieseite enthält Elemente, wie Verfeinerungen, kategorisierte Produktplatzierung und sortiert Optionen, enthält eine auserlesene Zusammenfassung und Paginierungskontrollen.</span><span class="sxs-lookup"><span data-stu-id="d0c10-106">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="d0c10-107">Allerdings anstatt die Standardkategorieseite zu verwenden, sollten Sie eine angereicherte Kategorieangebotsseite verwenden, die mehr Inhalt und mehr bestimmte Projekte aufweist.</span><span class="sxs-lookup"><span data-stu-id="d0c10-107">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="d0c10-108">Eine typische Bereicherung ist möglicherweise das Hinzufügen von kategoriespezifischen Marketings-Inhalt der Kategorieseite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="d0c10-108">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="d0c10-109">Dieser Inhalt kann überkreuzte Kategorieproduktplatzierungen enthalten für Cross-Sell-Zwecke, redaktionelle Listen, Bilder, Videos und anderen Text.</span><span class="sxs-lookup"><span data-stu-id="d0c10-109">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="d0c10-110">Sie können entweder die Standardkategorieseite ändern oder eine andere Kategorieseite für eine bestimmte Kategorie definieren.</span><span class="sxs-lookup"><span data-stu-id="d0c10-110">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Angereicherte Kategorie-Startseite](./media/CategoryLandingPages.png)

<span data-ttu-id="d0c10-112">Im Commerce Site Builder umfasst die Seite **Produkte** eine Liste der Kategorien vom Kanal, die dem Standort zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d0c10-112">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="d0c10-113">Wenn der Status **Angereichert** für eine Kategorieseite aktiviert ist, ist diese Kategorieseite angereichert worden.</span><span class="sxs-lookup"><span data-stu-id="d0c10-113">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="d0c10-114">Andernfalls werden die Standardkategorieseite und der Inhalt für die Kategorie verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0c10-114">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="d0c10-115">Sie können in der Vorschau angereicherte und nicht angereicherte Kategorieseiten für eine Kategorie anzeigen, wenn ein Kategoriename in der Liste ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="d0c10-115">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="d0c10-116">Um eine Kategorieseite anzureichern, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="d0c10-116">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="d0c10-117">Auf der Seite **Produkte** wählen Sie den Namen der Kategorie, für die Sie die Kategorieseite anreichern möchten.</span><span class="sxs-lookup"><span data-stu-id="d0c10-117">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="d0c10-118">Die Standardkategorieseite für die ausgewählte Kategorie ist im Seitenaufbereitungsprogramm geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d0c10-118">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="d0c10-119">Wählen Sie **Kategorieseite anreichern** aus.</span><span class="sxs-lookup"><span data-stu-id="d0c10-119">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="d0c10-120">Wählen Sie eine Vorlage für die angereicherte Kategorieseite aus.</span><span class="sxs-lookup"><span data-stu-id="d0c10-120">Select a template for the enriched category page.</span></span> <span data-ttu-id="d0c10-121">Wenn Sie nur geringfügige Änderungen vornehmen, können Sie die Standardkategorieseite auswählen.</span><span class="sxs-lookup"><span data-stu-id="d0c10-121">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="d0c10-122">Alternativ können Sie eine bestimmte Kategorieseitenvorlage auswählen.</span><span class="sxs-lookup"><span data-stu-id="d0c10-122">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="d0c10-123">Wenn Sie die Vorlage auswählen, ist das Seitenaufbereitungsprogramm geöffnet, und die ausgewählte Vorlage wird verwendet, um eine neue Kategorieseite für die ausgewählte Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d0c10-123">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="d0c10-124">Die Seite wird von Ihnen ausgecheckt und Sie können nun Ihre Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="d0c10-124">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="d0c10-125">Module, die Kategoriespezifikationsdaten verwenden, die Daten aus der ausgewählten Kategorie nutzen.</span><span class="sxs-lookup"><span data-stu-id="d0c10-125">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="d0c10-126">Die Einstellungen der Vorlage, die Sie auswählen, bestimmt die Änderungen, die Sie vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="d0c10-126">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d0c10-127">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d0c10-127">Additional resources</span></span>

[<span data-ttu-id="d0c10-128">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="d0c10-128">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="d0c10-129">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="d0c10-129">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d0c10-130">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="d0c10-130">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d0c10-131">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="d0c10-131">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="d0c10-132">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="d0c10-132">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d0c10-133">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="d0c10-133">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d0c10-134">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="d0c10-134">Verify page content accessibility</span></span>](verify-accessibility.md)

[<span data-ttu-id="d0c10-135">Dynamische E-Commerce-Seiten basierend auf URL-Parametern erstellen</span><span class="sxs-lookup"><span data-stu-id="d0c10-135">Create dynamic e-commerce pages based on URL parameters</span></span>](create-dynamic-pages.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
