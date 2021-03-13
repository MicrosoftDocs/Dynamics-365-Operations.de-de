---
title: Suchergebnismodul
description: Dieses Thema behandelt Suchergebnismodule und erläutert, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 3761be29955458099d01f2271057884fc1fd6f28
ms.sourcegitcommit: 872600103d2a444d78963867e5e0cdc62e68c3ec
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2021
ms.locfileid: "5097177"
---
# <a name="search-results-module"></a><span data-ttu-id="b55ac-103">Suchergebnismodul</span><span class="sxs-lookup"><span data-stu-id="b55ac-103">Search results module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="b55ac-104">Dieses Thema behandelt Suchergebnismodule und erläutert, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="b55ac-104">This topic covers search results modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="b55ac-105">Das Suchergebnismodul gibt Produktsuchergebnisse und eine Liste der anwendbaren Verfeinerungskriterien für die Produkte zurück.</span><span class="sxs-lookup"><span data-stu-id="b55ac-105">The search results module returns product search results and a list of applicable refiners for the products.</span></span> <span data-ttu-id="b55ac-106">Suchergebnismodule auf Dynamics 365 Commerce-Websites können zum Rendern von Seiten für folgende Szenarien verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="b55ac-106">Search results modules on Dynamics 365 Commerce sites can be used to render pages for the following scenarios:</span></span>

- <span data-ttu-id="b55ac-107">Suchergebnisse, die von einer Benutzersuche initiiert werden</span><span class="sxs-lookup"><span data-stu-id="b55ac-107">Search results that are initiated by a user search</span></span>
- <span data-ttu-id="b55ac-108">Suchergebnisse, die eine bestimmte Reihe von Produkten anzeigen, z. B. „Produkte mit ähnlichem Aussehen kaufen“</span><span class="sxs-lookup"><span data-stu-id="b55ac-108">Search results that show a specific set of products, such as "Shop similar looks"</span></span>
- <span data-ttu-id="b55ac-109">Eine Liste von Produkten, die zu einer bestimmten Kategorie gehören</span><span class="sxs-lookup"><span data-stu-id="b55ac-109">Lists of products that belong to a category</span></span>

<span data-ttu-id="b55ac-110">Weitere Informationen zu Kategorien- und Suchergebnisseiten finden Sie unter [Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite](category-search-page-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b55ac-110">For more information about category and search results pages, see [Default category landing page and search results page overview](category-search-page-overview.md).</span></span>

<span data-ttu-id="b55ac-111">Die folgende Abbildung zeigt das Beispiel einer Kategorie-Suchergebnisseite auf der Fabrikam-Website.</span><span class="sxs-lookup"><span data-stu-id="b55ac-111">The following illustration shows an example of a search results page for a category on the Fabrikam site.</span></span>

![Beispiel einer Suchergebnisseite auf der Fabrikam-Website](./media/SimpleCategoryLandingDressCategory.png)

## <a name="search-results-module-properties"></a><span data-ttu-id="b55ac-113">Eigenschaften des Suchergebnismoduls</span><span class="sxs-lookup"><span data-stu-id="b55ac-113">Search results module properties</span></span>

<span data-ttu-id="b55ac-114">In der folgenden Tabelle sind die Eigenschaften von Suchergebnismodulen mit ihren Werten und Beschreibungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b55ac-114">The following table lists the properties of search result modules, together with their values and descriptions.</span></span>

| <span data-ttu-id="b55ac-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="b55ac-115">Property</span></span> | <span data-ttu-id="b55ac-116">Werte</span><span class="sxs-lookup"><span data-stu-id="b55ac-116">Values</span></span> | <span data-ttu-id="b55ac-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b55ac-117">Description</span></span> |
|----------|--------|-------------|
| <span data-ttu-id="b55ac-118">Artikel pro Seite</span><span class="sxs-lookup"><span data-stu-id="b55ac-118">Items per page</span></span> | <span data-ttu-id="b55ac-119">Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="b55ac-119">Integer</span></span> | <span data-ttu-id="b55ac-120">Die Anzahl der Artikel, die auf jeder Seite angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-120">The number of items that should be shown on each page.</span></span> |
| <span data-ttu-id="b55ac-121">Wieder auf PDP zulassen</span><span class="sxs-lookup"><span data-stu-id="b55ac-121">Allow back on PDP</span></span> | <span data-ttu-id="b55ac-122">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="b55ac-122">**True** or **False**</span></span> | <span data-ttu-id="b55ac-123">Ist diese Eigenschaft auf **True** gesetzt, wird in der Breadcrumb-Navigation auf der geöffneten Produktdetailseite (Product Details Page, PDP) der Link „Zurück zu Ergebnissen“ angezeigt, wenn ein Benutzer ein Produkt auf der Suchergebnisseite auswählt.</span><span class="sxs-lookup"><span data-stu-id="b55ac-123">If this property is set to **True**, when a user selects a product on the search results page, the breadcrumb navigation on the product details page (PDP) that is opened will show a "Back to results" link.</span></span> |
| <span data-ttu-id="b55ac-124">Einschränkungen erweitern</span><span class="sxs-lookup"><span data-stu-id="b55ac-124">Expand Refiners</span></span> | <span data-ttu-id="b55ac-125">**Alle**, **1**, **2**, **3** oder **4**</span><span class="sxs-lookup"><span data-stu-id="b55ac-125">**All**, **1**, **2**, **3**, or **4**</span></span> | <span data-ttu-id="b55ac-126">Die Anzahl der Top-Verfeinerungskriterien, die beim Laden einer Seite erweitert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-126">The number of top refiners that should be expanded when a page is loaded.</span></span> <span data-ttu-id="b55ac-127">Beispielsweise werden die ersten drei Verfeinerungskriterien auf der Seite erweitert, wenn diese Eigenschaft auf **3** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="b55ac-127">For example, if this property is set to **3**, the first three refiners on the page will be expanded.</span></span> |
| <span data-ttu-id="b55ac-128">Kategorie-Hierarchieanzeige ausblenden</span><span class="sxs-lookup"><span data-stu-id="b55ac-128">Hide category hierarchy display</span></span> | <span data-ttu-id="b55ac-129">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="b55ac-129">**True** or **False**</span></span> | <span data-ttu-id="b55ac-130">Ist diese Eigenschaft auf **True** gesetzt, wird die Anzeige der Kategoriehierarchie auf der Seite ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="b55ac-130">If this property is set to **True**, the category hierarchy display on the page will be hidden.</span></span> <span data-ttu-id="b55ac-131">Diese Eigenschaft sollte auf **True** gesetzt sein, wenn Sie das [Breadcrumb-Modul](add-breadcrumb.md) nutzen, um die Kategoriehierarchie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-131">This property should be set to **True** if you're using the [breadcrumb module](add-breadcrumb.md) to show the category hierarchy.</span></span>|
| <span data-ttu-id="b55ac-132">Produktattribute in Suchergebnisse einbeziehen</span><span class="sxs-lookup"><span data-stu-id="b55ac-132">Include product attributes in search results</span></span> | <span data-ttu-id="b55ac-133">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="b55ac-133">**True** or **False**</span></span> | <span data-ttu-id="b55ac-134">Wenn diese Eigenschaft auf **True** gesetzt ist, werden für die Produkte in den Suchergebnissen Attribute zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b55ac-134">If this property is set to **True**, attributes will be returned for the products in the search results.</span></span> <span data-ttu-id="b55ac-135">Obwohl diese Attribute auf einer Commerce-Website angezeigt werden können, ist eine Erweiterung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b55ac-135">Although these attributes can be shown on a Commerce site, an extension is required.</span></span>|
| <span data-ttu-id="b55ac-136">Zugehörigkeitspreise anzeigen</span><span class="sxs-lookup"><span data-stu-id="b55ac-136">Show affiliation prices</span></span> | <span data-ttu-id="b55ac-137">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="b55ac-137">**True** or **False**</span></span> | <span data-ttu-id="b55ac-138">Ist diese Eigenschaft auf **True** gesetzt, werden in den Suchergebnissen Zugehörigkeitspreise für Produkte angezeigt, wenn ein angemeldeter Benutzer die Seite durchsucht.</span><span class="sxs-lookup"><span data-stu-id="b55ac-138">If this property is set to **True**, affiliation prices for products will be shown in the search results when a signed-in user browses the page.</span></span> |

> [!IMPORTANT]
> <span data-ttu-id="b55ac-139">In Dynamics 365 Commerce Version 10.0.16 und später kann die Konfiguration **Zugehörigkeitspreise anzeigen** verwendet werden, um die Zugehörigkeitspreise auf der Seite anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-139">In the Dynamics 365 Commerce 10.0.16 release and later, the **Show affiliation prices** configuration can be used to show affiliation prices on the page.</span></span>

## <a name="supported-modules"></a><span data-ttu-id="b55ac-140">Unterstützte Module</span><span class="sxs-lookup"><span data-stu-id="b55ac-140">Supported modules</span></span>

<span data-ttu-id="b55ac-141">Das Suchergebnismodul unterstützt das [Schnellansichtsmodul](quick-view-module.md), mit dem sich Benutzer Produktinformationen anzeigen lassen und Artikel über die Suchergebnisseite dem Warenkorb hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="b55ac-141">The search results module supports the [quick view module](quick-view-module.md), which lets users view product information and add items to the cart from the search results page.</span></span>

## <a name="add-a-search-results-module-to-a-category-page"></a><span data-ttu-id="b55ac-142">Einer Kategorieseite ein Suchergebnismodul hinzufügen</span><span class="sxs-lookup"><span data-stu-id="b55ac-142">Add a search results module to a category page</span></span>

<span data-ttu-id="b55ac-143">Führen Sie folgende Schritte aus, um ein Suchergebnismodul einer Kategorieseite hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-143">To add a search results module to a category page, follow these steps.</span></span>

1. <span data-ttu-id="b55ac-144">Wechseln Sie zu **Vorlagen** und wählen Sie **Neu** aus, um eine neue Vorlage zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-144">Go to **Templates**, and select **New** to create a new template.</span></span>
1. <span data-ttu-id="b55ac-145">Geben Sie im Dialogfeld **Neue Vorlage** den Namen **Suchergebnisse** ein, und wählen Sie anschließend **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-145">In the **New template** dialog box, enter the name **Search results**, and then select **OK**.</span></span>
1. <span data-ttu-id="b55ac-146">Wählen Sie im Slot **Körper** die Ellipsen-Schaltfläche (...) und anschließend **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-146">In the **Body** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b55ac-147">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Standardseite** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-147">In the **Add Module** dialog box, select the **Default Page** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b55ac-148">Wählen Sie im **Haupt**-Slot auf der **Standardseite** die Ellipsen-Schaltfläche (...) und anschließend **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-148">In the **Main** slot of the **Default Page** module, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b55ac-149">Wählen Sie im Dialogfeld **Modul hinzufügen** wählen Sie das Modul **Container** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-149">In the **Add Module** dialog box, select the **Container** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b55ac-150">Wählen Sie im **Container**-Slot die Ellipsen-Schaltfläche (...) und anschließend **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-150">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b55ac-151">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Breadcrumb** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-151">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b55ac-152">Geben Sie im **Breadcrumb**-Eigenschaftenbereich den Wert **1** für **Min. Vorkommen** ein.</span><span class="sxs-lookup"><span data-stu-id="b55ac-152">In the **Breadcrumb** properties pane, enter the value **1** for **Min Occurs**.</span></span>
1. <span data-ttu-id="b55ac-153">Wählen Sie im **Container**-Slot die Ellipsen-Schaltfläche (...) und anschließend **Modul hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-153">In the **Container** slot, select the ellipsis (...), and then select **Add Module**.</span></span>
1. <span data-ttu-id="b55ac-154">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Suchergebnisse** und anschließend **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-154">In the **Add Module** dialog box, select the **Search results** module, and then select **OK**.</span></span>
1. <span data-ttu-id="b55ac-155">Geben Sie im **Suchergebnisse**-Eigenschaftenbereich den Wert **1** für **Min. Vorkommen** ein, und legen Sie dann alle anderen erforderlichen Eigenschaften für das Suchergebnismodul fest.</span><span class="sxs-lookup"><span data-stu-id="b55ac-155">In the **Search results** properties pane, enter the value **1** for **Min Occurs**, and then set any other required properties for the search results module.</span></span> <span data-ttu-id="b55ac-156">Durch Festlegen dieser Eigenschaften in der Vorlage stellen Sie sicher, dass alle Anpassungen auf einer bestimmten Kategorieseite diese Einstellungen automatisch enthalten.</span><span class="sxs-lookup"><span data-stu-id="b55ac-156">By setting these properties in the template, you ensure that any customizations to a specific category page will automatically include these settings.</span></span>
1. <span data-ttu-id="b55ac-157">Wählen Sie **Bearbeiten beenden** aus, und wählen Sie dann **Veröffentlichen** aus, um die Vorlage zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-157">Select **Finish editing**, and then select **Publish** to publish the template.</span></span>
1. <span data-ttu-id="b55ac-158">Wechseln Sie zu **Seiten**, und wählen Sie dann **Neu** aus, um eine neue Seite zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-158">Go to **Pages**, and select **New** to create a new page.</span></span>
1. <span data-ttu-id="b55ac-159">Wählen Sie im Dialogfeld **Vorlage auswählen** die zuvor erstellte **Suchergebnis**-Vorlage aus. Geben Sie als **Seitenname** **Kategorieseite** ein, und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="b55ac-159">In the **Choose a template** dialog box, select the **Search results** template that you created, enter **Category page** for **Page name**, and then select **OK**.</span></span> <span data-ttu-id="b55ac-160">Da alle Werte in der Vorlage festgelegt sind, kann die Seite veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="b55ac-160">Because all the values are set in the template, the page is ready to be published.</span></span>
1. <span data-ttu-id="b55ac-161">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="b55ac-161">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b55ac-162">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b55ac-162">Additional resources</span></span>

[<span data-ttu-id="b55ac-163">Übersicht zur Zielseite der Standardkategorie und der Suchergebnisseite</span><span class="sxs-lookup"><span data-stu-id="b55ac-163">Default category landing page and search results page overview</span></span>](category-search-page-overview.md)

[<span data-ttu-id="b55ac-164">Informationen zur Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="b55ac-164">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="b55ac-165">Schnellansichtsmodul</span><span class="sxs-lookup"><span data-stu-id="b55ac-165">Quick view module</span></span>](quick-view-module.md)
