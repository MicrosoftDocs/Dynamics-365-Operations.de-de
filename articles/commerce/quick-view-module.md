---
title: Schnellansichtsmodul
description: Dieses Thema enthält Schnellansichtsmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-01-08
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: d7e88163fd9b8dc4f5636ed29e2c4248aece52bf
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792170"
---
# <a name="quick-view-module"></a><span data-ttu-id="5d4e6-103">Schnellansichtsmodul</span><span class="sxs-lookup"><span data-stu-id="5d4e6-103">Quick view module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="5d4e6-104">Dieses Thema enthält Schnellansichtsmodule und es wird beschrieben, wie diese Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-104">This topic covers quick view modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="5d4e6-105">Mit dem Schnellansichtsmodul können Benutzer Produktinformationen schnell anzeigen, wenn sie Produkte auf einer Listenseite durchsuchen und ein oder mehrere Produkte über die Listenseite zum Warenkorb hinzufügen, ohne zur Produktdetailseite (PDP) wechseln zu müssen.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-105">The quick view module lets users quickly view product information when they browse products on a list page, and add one or more products to the cart from the list page, without having to go to the product details page (PDP).</span></span> <span data-ttu-id="5d4e6-106">Das Schnellansichtsmodul bietet einen Überblick über die Produktinformationen, die Benutzer benötigen, um eine Entscheidung zum Hinzufügen zum Warenkorb zu treffen.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-106">The quick view module provides an overview of the product information that users require to make an "add to cart" decision.</span></span> <span data-ttu-id="5d4e6-107">Es enthält auch einen Link zum PDP, sodass Benutzer zusätzliche Produktdetails und Kaufoptionen anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-107">It also provides a link to the PDP, so that users can view additional product details and purchase options.</span></span>

<span data-ttu-id="5d4e6-108">Das Schnellansichtsmodul wird von den Modulen [Produktkollektion](product-collection-module-overview.md) und [Suchergebnisse](search-result-module.md) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-108">The quick view module is supported by the [product collection](product-collection-module-overview.md) and [search results](search-result-module.md) modules.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5d4e6-109">Das Schnellansichtsmodul ist ab der Version 10.0.17 von Commerce verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-109">The quick view module is available as of the Commerce version 10.0.17 release.</span></span>

<span data-ttu-id="5d4e6-110">Das folgende Bild zeigt ein Beispiel eines Schnellansichtsmoduls auf einer Produktlistenseite.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-110">The following illustration shows an example of a quick view module on a product list page.</span></span>

![Beispiel eines Schnellansichtsmoduls auf einer Produktlistenseite](./media/ecommerce-quickview.PNG)

## <a name="module-properties"></a><span data-ttu-id="5d4e6-112">Moduleigenschaften</span><span class="sxs-lookup"><span data-stu-id="5d4e6-112">Module properties</span></span>

<span data-ttu-id="5d4e6-113">Das Schnellansichtsmodul unterstützt einige der gleichen Funktionen wie das Kauffeldmodul.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-113">The quick view module supports some of the same functions as the buy box module.</span></span> <span data-ttu-id="5d4e6-114">Daher ähneln die Eigenschaften eines Schnellansichtsmoduls den Eigenschaften eines Kauffeldmoduls.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-114">Therefore, the properties of a quick view module resemble the properties of a buy box module.</span></span>

| <span data-ttu-id="5d4e6-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="5d4e6-115">Property</span></span> | <span data-ttu-id="5d4e6-116">Werte</span><span class="sxs-lookup"><span data-stu-id="5d4e6-116">Values</span></span> | <span data-ttu-id="5d4e6-117">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d4e6-117">Description</span></span> |
|----------------|--------|-------------|
| <span data-ttu-id="5d4e6-118">Überschriften-Tag</span><span class="sxs-lookup"><span data-stu-id="5d4e6-118">Heading tag</span></span> | <span data-ttu-id="5d4e6-119">**H1**, **H2**, **H3**, **H4**, **H5** oder **H6**</span><span class="sxs-lookup"><span data-stu-id="5d4e6-119">**H1**, **H2**, **H3**, **H4**, **H5**, or **H6**</span></span> | <span data-ttu-id="5d4e6-120">Diese Eigenschaft definiert das Überschriften-Tag für den Produkttitel.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-120">This property defines the heading tag for the product title.</span></span> <span data-ttu-id="5d4e6-121">Wenn sich das Schnellansichtsmodul oben auf der Seite befindet, sollte diese Eigenschaft auf **H1** festgelegt werden, um die Zugänglichkeitsstandards zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-121">If the quick view module is at the top of the page, this property should be set to **H1** to meet accessibility standards.</span></span> |
| <span data-ttu-id="5d4e6-122">Benutzerdefinierten Preis zulassen</span><span class="sxs-lookup"><span data-stu-id="5d4e6-122">Allow custom price</span></span> | <span data-ttu-id="5d4e6-123">**True** oder **False**</span><span class="sxs-lookup"><span data-stu-id="5d4e6-123">**True** or **False**</span></span> | <span data-ttu-id="5d4e6-124">Wenn diese Eigenschaft auf **Wahr** gesetzt ist, kann der Benutzer einen benutzerdefinierten Preis eingeben.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-124">If this property is set to **True**, the user can enter a custom price.</span></span> |
| <span data-ttu-id="5d4e6-125">Minimaler Preis</span><span class="sxs-lookup"><span data-stu-id="5d4e6-125">Minimum price</span></span> | <span data-ttu-id="5d4e6-126">Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="5d4e6-126">Integer</span></span> | <span data-ttu-id="5d4e6-127">Diese Eigenschaft gilt nur, wenn die **Benutzerdefinierten Preis zulassen**-Eigenschaft auf **Wahr** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-127">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="5d4e6-128">Es definiert den Mindestpreis, den der Benutzer eingeben kann (z. B. 1 USD).</span><span class="sxs-lookup"><span data-stu-id="5d4e6-128">It defines the minimum price that the user can enter (for example, $1).</span></span> |
| <span data-ttu-id="5d4e6-129">Maximaler Preis</span><span class="sxs-lookup"><span data-stu-id="5d4e6-129">Maximum price</span></span> | <span data-ttu-id="5d4e6-130">Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="5d4e6-130">Integer</span></span> | <span data-ttu-id="5d4e6-131">Diese Eigenschaft gilt nur, wenn die **Benutzerdefinierten Preis zulassen**-Eigenschaft auf **Wahr** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-131">This property is applicable only if the **Allow custom price** property is set to **True**.</span></span> <span data-ttu-id="5d4e6-132">Es definiert den Maximalpreis, den der Benutzer eingeben kann (z. B. 1.000 USD).</span><span class="sxs-lookup"><span data-stu-id="5d4e6-132">It defines the maximum price that the user can enter (for example, $1,000).</span></span> |

## <a name="commerce-site-builder-settings"></a><span data-ttu-id="5d4e6-133">Commerce-Website-Generator-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="5d4e6-133">Commerce site builder settings</span></span>

<span data-ttu-id="5d4e6-134">Wie das Kauffeldmodul berücksichtigt auch das Schnellansichtsmodul die Einstellungen unter **Seiteneinstellungen \> Erweiterungen \> Produkt in den Warenkorb legen**.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-134">Like the buy box module, the quick view module respects the settings at **Site Settings \> Extensions \> Add product to cart**.</span></span> <span data-ttu-id="5d4e6-135">Die **Zur Warenkorbseite navigieren**-Einstellung wird ignoriert, da sie nicht mit dem Zweck des Schnellansichtsmoduls übereinstimmt, mit dem Benutzer mehrere Produkte auf einer Listenseite durchsuchen und in den Warenkorb legen können, ohne sich von der Listenseite zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-135">However, the **Navigate to cart page** setting is ignored, because it's inconsistent with the purpose of the quick view module, which is to enable users to browse multiple products on a list page and add them to the cart without moving away from the list page.</span></span>

## <a name="add-a-quick-view-module-to-a-product-collection-module"></a><span data-ttu-id="5d4e6-136">Hinzufügen eines Schnellansichtsmoduls zu einem Produktsammlungsmodul</span><span class="sxs-lookup"><span data-stu-id="5d4e6-136">Add a quick view module to a product collection module</span></span>

<span data-ttu-id="5d4e6-137">Ein Schnellansichtsmodul kann den Modulen Produktkollektion und Suchergebnisse hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-137">A quick view module can be added to the product collection and search results modules.</span></span>

<span data-ttu-id="5d4e6-138">Gehen Sie folgendermaßen vor, um ein Schnellansichtsmodul im Commerce-Website-Generator einem Produktsammlungsmodul hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-138">To add a quick view module to a product collection module in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="5d4e6-139">Rufen Sie **Seiten** auf und wählen Sie dann die Startseite für die Fabrikam-Website aus.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-139">Go to **Pages**, and then select the home page for the Fabrikam site.</span></span>
1. <span data-ttu-id="5d4e6-140">Gehen Sie zu einem **Produktsammlungs**-Modul auf der Startseite, wählen Sie die Auslassungspunkte (**...**) und wählen Sie dann **Modul hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-140">Go to any **Product Collection** module on the homepage, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="5d4e6-141">Wählen Sie im Dialogfeld **Modul hinzufügen** das Modul **Schnellansicht** und dann **OK** aus.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-141">In the **Add Module** dialog box, select the **Quick View** module, and then select **OK**.</span></span>
1. <span data-ttu-id="5d4e6-142">Im Eigenschaftenbereich des **Schnellansicht**-Moduls wählen Sie **Überschrift**.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-142">In the properties pane of the **Quick View** module, select **Heading**.</span></span> <span data-ttu-id="5d4e6-143">Im **Überschrift**-Dialogfeld stellen Sie das **Überschriftenebene**-Feld auf **H2** und wählen dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-143">In the **Heading** dialog box, set the **Heading Level** field to **H2**, and then select **OK**.</span></span>
1. <span data-ttu-id="5d4e6-144">Wählen Sie **Speichern**, wählen Sie **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um es zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="5d4e6-144">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5d4e6-145">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5d4e6-145">Additional resources</span></span>

[<span data-ttu-id="5d4e6-146">Informationen zur Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="5d4e6-146">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="5d4e6-147">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="5d4e6-147">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="5d4e6-148">Produktsammelmodul</span><span class="sxs-lookup"><span data-stu-id="5d4e6-148">Product collection module</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="5d4e6-149">Suchergebnismodul</span><span class="sxs-lookup"><span data-stu-id="5d4e6-149">Search results module</span></span>](search-result-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
