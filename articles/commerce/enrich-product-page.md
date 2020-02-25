---
title: Erweitern einer Produktseite
description: In diesem Thema wird beschrieben, wie eine Produktseite in Microsoft Dynamics 365 Commerce ergänzt wird.
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
ms.openlocfilehash: d4c495fc6dfe4aa6561a1bb703253ef8ec71dc13
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003072"
---
# <a name="enrich-a-product-page"></a><span data-ttu-id="473b6-103">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="473b6-103">Enrich a product page</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="473b6-104">In diesem Thema wird beschrieben, wie eine Produktseite in Microsoft Dynamics 365 Commerce ergänzt wird.</span><span class="sxs-lookup"><span data-stu-id="473b6-104">This topic describes how to enrich a product page in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="473b6-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="473b6-105">Overview</span></span>

<span data-ttu-id="473b6-106">Standardmäßig verwendet Ihr Standort eine generische Seite, um Produktdaten anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="473b6-106">By default, your site uses a generic page to show product data.</span></span> <span data-ttu-id="473b6-107">Diese Seite enthält die grundlegenden Informationen zu Produktpreisen und Steuerelementen, die erforderlich sind, um es zu verkaufen.</span><span class="sxs-lookup"><span data-stu-id="473b6-107">This page includes the basic information about the product and the controls that are required to sell it.</span></span> <span data-ttu-id="473b6-108">Sie können jedoch die Informationen, die über die Commerce-Skalierungseinheit kommen, durch zusätzliche Bilder oder Texte für ein bestimmtes Produkt ergänzen.</span><span class="sxs-lookup"><span data-stu-id="473b6-108">However, you can supplement the information that comes from the Commerce Scale Unit with additional images or text for a specific product.</span></span> <span data-ttu-id="473b6-109">Dieser Vorgang wird als Anreicherung der Produktseite bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="473b6-109">This process is known as enriching the product page.</span></span>

<span data-ttu-id="473b6-110">In vielen Fällen möchten Sie bestimmten zusätzlichen Inhalt für Ihre Produkte verwenden.</span><span class="sxs-lookup"><span data-stu-id="473b6-110">In many cases, you will want to use specific additional content for your products.</span></span> <span data-ttu-id="473b6-111">Wenn Sie zu **Retail und Commerce** im Erstellungstool wechseln, sehen Sie eine Liste von Produkten von dem Kanal, der der Site zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="473b6-111">When you go to **Retail and Commerce** in the authoring tool, you will see a list of products from the channel that is assigned to the site.</span></span> <span data-ttu-id="473b6-112">In dieser Liste zeigen die Spalten **Angereichert** an, ob die Produktseite für ein Produkt angereichert wurde.</span><span class="sxs-lookup"><span data-stu-id="473b6-112">In this list, the **Enriched** column indicates whether the product page for a product has been enriched.</span></span> <span data-ttu-id="473b6-113">Wenn ein Häkchen in der Spalte angezeigt wird, liegt eine angereicherte Produktseite für das Produkt vor.</span><span class="sxs-lookup"><span data-stu-id="473b6-113">If a check mark appears in the column, an enriched product page exists for the product.</span></span> <span data-ttu-id="473b6-114">Wenn kein Häkchen angezeigt wird, werden die Standardproduktseite und -Inhalt für das Produkt verwendet.</span><span class="sxs-lookup"><span data-stu-id="473b6-114">If no check mark appears, the default product page and content are used for the product.</span></span> <span data-ttu-id="473b6-115">Sie können in der Vorschau angereicherte und nicht angereicherte Produktseiten anzeigen, wenn ein Produktname in der Liste ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="473b6-115">You can preview both enriched and non-enriched product pages by selecting a product name in the list.</span></span>

## <a name="enrich-a-product-page"></a><span data-ttu-id="473b6-116">Erweitern einer Produktseite</span><span class="sxs-lookup"><span data-stu-id="473b6-116">Enrich a product page</span></span>

<span data-ttu-id="473b6-117">Um ein Produktseite anzureichern, führen Sie die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-117">To enrich a product page, follow these steps.</span></span>

1. <span data-ttu-id="473b6-118">Wählen Sie unter **Sites** **Fabrikam** (oder den Namen Ihrer Site) aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-118">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="473b6-119">Wählen Sie im linken Navigationsbereich **Produkte** aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-119">In the navigation pane on the left, select **Products**.</span></span>
1. <span data-ttu-id="473b6-120">Wählen Sie ein beliebiges Produkt aus, das keine angereicherte Produktseite hat.</span><span class="sxs-lookup"><span data-stu-id="473b6-120">Select any product that doesn't have an enriched product page.</span></span>
1. <span data-ttu-id="473b6-121">Klicken Sie im Aktivitätsbereich auf **Produktseite anreichern**.</span><span class="sxs-lookup"><span data-stu-id="473b6-121">On the Action Pane, select **Enrich product page**.</span></span>
1. <span data-ttu-id="473b6-122">Wählen Sie **PDP-Vorlage** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-122">Select **PDP-template**, and then select **OK**.</span></span>
1. <span data-ttu-id="473b6-123">In der Seitengliederungsstruktur im Feld links, erweitern Sie den **Haupt-** Slot.</span><span class="sxs-lookup"><span data-stu-id="473b6-123">In the page outline tree on the left, expand the **Main** slot.</span></span>
1. <span data-ttu-id="473b6-124">Wählen Sie die Ellipsen-Schaltfläche (**...**) für den **Haupt-** Slot und wählen Sie **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="473b6-124">Select the ellipsis button (**...**) for the **Main** slot, and then select **Add Module**.</span></span>
1. <span data-ttu-id="473b6-125">Wählen Sie **Container 2** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-125">Select **Container 2**, and then select **OK**.</span></span>
1. <span data-ttu-id="473b6-126">Wählen Sie die Ellipsen-Schaltfläche für den **Container 2** und wählen Sie dann **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="473b6-126">Select the ellipsis button for **Container 2**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="473b6-127">Wählen Sie **Funktion** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-127">Select **Feature**, and then select **OK**.</span></span>
1. <span data-ttu-id="473b6-128">Im Eigenschaftenbereich auf der rechten Seite, im Feld **Rich-Text** geben Sie die aktualisierte Beschreibung des Produkts ein.</span><span class="sxs-lookup"><span data-stu-id="473b6-128">In the properties pane on the right, in the **Rich Text** field, enter the updated description of the product.</span></span>
1. <span data-ttu-id="473b6-129">Geben Sie im Feld **Kopf** eine Überschrift ein und wählen dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-129">In the **Heading** field, enter heading text, and then select **OK**.</span></span>
1. <span data-ttu-id="473b6-130">Wählen Sie **Speichern** und dann **Hochladen** aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-130">Select **Save**, and then select **Check In**.</span></span>
1. <span data-ttu-id="473b6-131">Geben Sie im Feld **Kommentare** **Angereichertes Produkt** ein und wählen Sie dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-131">In the **Comments** field, enter **Enriched a product**, and then select **OK**.</span></span>
1. <span data-ttu-id="473b6-132">Wählen Sie **Vorschau** aus, um die aktualisierte Produkteite in der Vorschau anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="473b6-132">Select **Preview** to preview the enriched product page.</span></span> <span data-ttu-id="473b6-133">Wenn Sie fertig sind, schließen Sie die Vorschauregisterkarte, um zum Erstellungstool zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="473b6-133">When you've finished, close the preview tab to return to the authoring tool.</span></span>
1. <span data-ttu-id="473b6-134">Wählen Sie **Veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="473b6-134">Select **Publish**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="473b6-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="473b6-135">Additional resources</span></span>

[<span data-ttu-id="473b6-136">Bestehende Seite einer Website ändern</span><span class="sxs-lookup"><span data-stu-id="473b6-136">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="473b6-137">Neue Seite hinzufügen</span><span class="sxs-lookup"><span data-stu-id="473b6-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="473b6-138">Auswählen von Seitenlayouts</span><span class="sxs-lookup"><span data-stu-id="473b6-138">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="473b6-139">Verwalten von SEO-Metadaten</span><span class="sxs-lookup"><span data-stu-id="473b6-139">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="473b6-140">Speichern, Vorschau und Veröffentlichung einer Seite</span><span class="sxs-lookup"><span data-stu-id="473b6-140">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="473b6-141">Füllen einer Kategorie-Landingpage</span><span class="sxs-lookup"><span data-stu-id="473b6-141">Enrich a category landing page</span></span>](enrich-category-page.md)

[<span data-ttu-id="473b6-142">Überprüfen der Zugänglichkeit des Seiteninhalts</span><span class="sxs-lookup"><span data-stu-id="473b6-142">Verify page content accessibility</span></span>](verify-accessibility.md)
