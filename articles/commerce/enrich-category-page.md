---
title: Füllen einer Kategorie-Landingpage
description: In diesem Thema wird die Anreicherung der Kategorieseiten in Dynamics 365 Commerce abgedeckt.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
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
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: ca31ec7d2eee7d2b0c863506338341a870ff07ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4412565"
---
# <a name="enrich-a-category-landing-page"></a><span data-ttu-id="1f577-103">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="1f577-103">Enrich a category landing page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="1f577-104">In diesem Thema wird die Anreicherung der Kategorieseiten in Dynamics 365 Commerce abgedeckt.</span><span class="sxs-lookup"><span data-stu-id="1f577-104">This topic covers the enrichment of category pages in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="1f577-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="1f577-105">Overview</span></span>

<span data-ttu-id="1f577-106">Handel enthält eine Standardkategorieangebotsseite, die verwendet wird, wenn Kategoriedaten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="1f577-106">Commerce provides a default category landing page that is used when category data is shown.</span></span> <span data-ttu-id="1f577-107">Eine obligatorische Standardkategorieseite enthält Elemente, wie Verfeinerungen, kategorisierte Produktplatzierung und sortiert Optionen, enthält eine auserlesene Zusammenfassung und Paginierungskontrollen.</span><span class="sxs-lookup"><span data-stu-id="1f577-107">A default category page contains required elements, such as refiners, categorized product placement, sorting options, a choice summary, and pagination controls.</span></span> 

<span data-ttu-id="1f577-108">Allerdings anstatt die Standardkategorieseite zu verwenden, sollten Sie eine angereicherte Kategorieangebotsseite verwenden, die mehr Inhalt und mehr bestimmte Projekte aufweist.</span><span class="sxs-lookup"><span data-stu-id="1f577-108">However, instead of using the default category page, you might want to use an "enriched" category landing page that has more content and more specific elements.</span></span> <span data-ttu-id="1f577-109">Eine typische Bereicherung ist möglicherweise das Hinzufügen von kategoriespezifischen Marketings-Inhalt der Kategorieseite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1f577-109">A typical enrichment might involve adding category-specific marketing content to the category page.</span></span> <span data-ttu-id="1f577-110">Dieser Inhalt kann überkreuzte Kategorieproduktplatzierungen enthalten für Cross-Sell-Zwecke, redaktionelle Listen, Bilder, Videos und anderen Text.</span><span class="sxs-lookup"><span data-stu-id="1f577-110">This content might include cross-category product placement for cross-sell purposes, editorial lists, images, videos, and other text.</span></span> <span data-ttu-id="1f577-111">Sie können entweder die Standardkategorieseite ändern oder eine andere Kategorieseite für eine bestimmte Kategorie definieren.</span><span class="sxs-lookup"><span data-stu-id="1f577-111">You can either modify the default category page or define a different category page for a specific category.</span></span>

![Angereicherte Kategorie-Startseite](./media/CategoryLandingPages.png)

<span data-ttu-id="1f577-113">Im Commerce Site Builder umfasst die Seite **Produkte** eine Liste der Kategorien vom Kanal, die dem Standort zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="1f577-113">In Commerce site builder, the **Products** page includes a list of categories from the channel that are assigned to the site.</span></span> <span data-ttu-id="1f577-114">Wenn der Status **Angereichert** für eine Kategorieseite aktiviert ist, ist diese Kategorieseite angereichert worden.</span><span class="sxs-lookup"><span data-stu-id="1f577-114">If the **Enriched** status is selected for a category page, that category page has been enriched.</span></span> <span data-ttu-id="1f577-115">Andernfalls werden die Standardkategorieseite und der Inhalt für die Kategorie verwendet.</span><span class="sxs-lookup"><span data-stu-id="1f577-115">Otherwise, the default category page and content are used for the category.</span></span> <span data-ttu-id="1f577-116">Sie können in der Vorschau angereicherte und nicht angereicherte Kategorieseiten für eine Kategorie anzeigen, wenn ein Kategoriename in der Liste ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="1f577-116">You can preview both the enriched and non-enriched category pages for a category by selecting the category name.</span></span>

<span data-ttu-id="1f577-117">Um eine Kategorieseite anzureichern, gehen Sie folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="1f577-117">To enrich a category page, do the following.</span></span>

1. <span data-ttu-id="1f577-118">Auf der Seite **Produkte** wählen Sie den Namen der Kategorie, für die Sie die Kategorieseite anreichern möchten.</span><span class="sxs-lookup"><span data-stu-id="1f577-118">On the **Products** page, select the name of the category for which you want to enrich the category page.</span></span> <span data-ttu-id="1f577-119">Die Standardkategorieseite für die ausgewählte Kategorie ist im Seitenaufbereitungsprogramm geöffnet.</span><span class="sxs-lookup"><span data-stu-id="1f577-119">The default category page for the selected category is opened in the page editor.</span></span>
2. <span data-ttu-id="1f577-120">Wählen Sie **Kategorieseite anreichern** aus.</span><span class="sxs-lookup"><span data-stu-id="1f577-120">Select **Enrich category page**.</span></span>
3. <span data-ttu-id="1f577-121">Wählen Sie eine Vorlage für die angereicherte Kategorieseite aus.</span><span class="sxs-lookup"><span data-stu-id="1f577-121">Select a template for the enriched category page.</span></span> <span data-ttu-id="1f577-122">Wenn Sie nur geringfügige Änderungen vornehmen, können Sie die Standardkategorieseite auswählen.</span><span class="sxs-lookup"><span data-stu-id="1f577-122">If you're making only minor changes, you can select the default category page.</span></span> <span data-ttu-id="1f577-123">Alternativ können Sie eine bestimmte Kategorieseitenvorlage auswählen.</span><span class="sxs-lookup"><span data-stu-id="1f577-123">Alternatively, you can select a specific category page template.</span></span> <span data-ttu-id="1f577-124">Wenn Sie die Vorlage auswählen, ist das Seitenaufbereitungsprogramm geöffnet, und die ausgewählte Vorlage wird verwendet, um eine neue Kategorieseite für die ausgewählte Kategorie zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="1f577-124">When you select the template, the page editor is opened, and the selected template is used to create a new category page for the selected category.</span></span> <span data-ttu-id="1f577-125">Die Seite wird von Ihnen ausgecheckt und Sie können nun Ihre Änderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="1f577-125">The page is checked out to you, and you can now make your changes.</span></span>

> [!NOTE]
> <span data-ttu-id="1f577-126">Module, die Kategoriespezifikationsdaten verwenden, die Daten aus der ausgewählten Kategorie nutzen.</span><span class="sxs-lookup"><span data-stu-id="1f577-126">Modules that use category specification data use the data from your selected category.</span></span> <span data-ttu-id="1f577-127">Die Einstellungen der Vorlage, die Sie auswählen, bestimmt die Änderungen, die Sie vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="1f577-127">The settings of the template that you select determine the changes that you can make.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f577-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1f577-128">Additional resources</span></span>

[<span data-ttu-id="1f577-129">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="1f577-129">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="1f577-130">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="1f577-130">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="1f577-131">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="1f577-131">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="1f577-132">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="1f577-132">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="1f577-133">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="1f577-133">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="1f577-134">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="1f577-134">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="1f577-135">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="1f577-135">Verify page content accessibility</span></span>](verify-accessibility.md)
