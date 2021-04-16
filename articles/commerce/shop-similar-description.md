---
title: Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ aktivieren
description: In diesem Thema wird beschrieben, wie Sie Produktempfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ in Microsoft Dynamics 365 Commerce aktivieren.
author: bsokolov
ms.date: 01/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: ce01ef1d4b916d955685b4d01dafd3d54d6fcebd
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795404"
---
# <a name="enable-shop-similar-description-recommendations"></a><span data-ttu-id="de94b-103">Empfehlungen zu „Artikel mit ähnlicher Beschreibung kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="de94b-103">Enable "shop similar description" recommendations</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="de94b-104">In diesem Thema wird beschrieben, wie Sie Produktempfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ in Microsoft Dynamics 365 Commerce aktivieren.</span><span class="sxs-lookup"><span data-stu-id="de94b-104">This topic describes how to enable "shop similar description" product recommendations in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="de94b-105">Die Empfehlungsfunktion für „Produkte mit ähnlicher Beschreibung kaufen“ in Dynamics 365 Commerce nutzt die künstliche Intelligenz und maschinelles Lernen (KI-ML), um Kunden Empfehlungen für Produkte liefern, deren Beschreibung dem ähnelt, wonach der Kunde sucht.</span><span class="sxs-lookup"><span data-stu-id="de94b-105">The "shop similar description" recommendations feature in Dynamics 365 Commerce uses artificial intelligence and machine learning (AI-ML) to deliver recommendations for products that have descriptions that are similar to what the customer is looking for.</span></span> <span data-ttu-id="de94b-106">Durch die Bereitstellung von Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ für alle Einzelhandelskanäle in Commerce können Einzelhändler Kunden dabei helfen, leicht zu finden, wonach sie suchen.</span><span class="sxs-lookup"><span data-stu-id="de94b-106">By making "shop similar description" recommendations available for all retail channels in Commerce, retailers can help customers easily find what they want.</span></span>

<span data-ttu-id="de94b-107">Die Funktionalität für Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ verwendet den Produktnamen und die Beschreibung von Startproduktvarianten, um ähnliche Produkte im Produktkatalog eines Einzelhändlers zu finden und zu empfehlen.</span><span class="sxs-lookup"><span data-stu-id="de94b-107">The functionality for "shop similar description" recommendations uses the product name and description of seed products to find and recommend similar products in a retailer's product catalog.</span></span>

<span data-ttu-id="de94b-108">Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ sind sowohl in POS‑ als auch in E-Commerce-Umgebungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="de94b-108">"Shop similar description" recommendations are available in both the point of sale (POS) and e-commerce experiences.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="de94b-109">Beispielszenarien</span><span class="sxs-lookup"><span data-stu-id="de94b-109">Example scenarios</span></span>

<span data-ttu-id="de94b-110">Die folgenden Beispielszenarien zeigen die Empfehlungstypen, die die Funktion „Produkte mit Ähnlicher Beschreibung kaufen“ bieten kann:</span><span class="sxs-lookup"><span data-stu-id="de94b-110">The following example scenarios show the types of recommendations that the "shop similar description" functionality can provide:</span></span>

- <span data-ttu-id="de94b-111">Ein Kunde betrachtet eine Hornbrille im Retro-Stil und erhält eine Reihe von Empfehlungen für andere Brillen mit ähnlichem Design im Kontext der Einzelhandelsbranche.</span><span class="sxs-lookup"><span data-stu-id="de94b-111">A customer views a pair of retro-style horn-rimmed glasses and receives a set of recommendations for other glasses that have a similar design, in the context of the retailer's industry.</span></span>
- <span data-ttu-id="de94b-112">Ein Kunde verwendet die Empfehlungen „Produkte mit ähnlicher Beschreibung kaufen“, um Kaffeearomen zu entdecken, die einem Aroma ähneln, das er zuvor beim Einzelhändler gekauft hat.</span><span class="sxs-lookup"><span data-stu-id="de94b-112">A customer uses "shop similar description" recommendations to discover coffee flavors that are similar to a flavor that they previously purchased from the retailer.</span></span>

## <a name="set-up-shop-similar-description-recommendations"></a><span data-ttu-id="de94b-113">Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ einrichten</span><span class="sxs-lookup"><span data-stu-id="de94b-113">Set up "shop similar description" recommendations</span></span>

<span data-ttu-id="de94b-114">Produktempfehlungen werden nur für Commerce-Benutzer unterstützt, die ihren Speicher zu Azure Data Lake Storage Gen2 migriert haben.</span><span class="sxs-lookup"><span data-stu-id="de94b-114">Product recommendations are supported only for Commerce users who have migrated their storage to Azure Data Lake Storage Gen2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="de94b-115">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="de94b-115">Prerequisites</span></span>

<span data-ttu-id="de94b-116">Bevor den Kunden Empfehlungen für „Produkte mit ähnlicher Beschreibung kaufen“ angezeigt werden können, müssen Sie die folgenden Voraussetzungen befolgen:</span><span class="sxs-lookup"><span data-stu-id="de94b-116">Before "shop similar description" recommendations can be shown to customers, you must complete the following prerequisites:</span></span>

- <span data-ttu-id="de94b-117">[Produktempfehlungen aktivieren](enable-product-recommendations.md) in der Commerce-Zentrale.</span><span class="sxs-lookup"><span data-stu-id="de94b-117">[Enable product recommendations](enable-product-recommendations.md) in Commerce headquarters.</span></span>
- <span data-ttu-id="de94b-118">Stellen Sie sicher, dass der Medienserver HTTPS-Aufrufe unterstützt.</span><span class="sxs-lookup"><span data-stu-id="de94b-118">Confirm that the media server supports HTTPS calls.</span></span>

### <a name="turn-on-the-shop-similar-description-recommendations-feature"></a><span data-ttu-id="de94b-119">Empfehlungsfunktion für „Produkte mit ähnlicher Beschreibung kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="de94b-119">Turn on the "shop similar description" recommendations feature</span></span>

<span data-ttu-id="de94b-120">Führen Sie die folgenden Schritte aus, um die Empfehlungsfunktion „Produkte mit ähnlicher Beschreibung kaufen“ in der Commerce-Zentralverwaltung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="de94b-120">To turn on the "shop similar description" recommendations feature in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="de94b-121">Suchen und wählen Sie im Arbeitsbereich **Funktionsverwaltung** in der Liste der verfügbaren Funktionen **Produkte mit ähnlicher Beschreibung kaufen** aus.</span><span class="sxs-lookup"><span data-stu-id="de94b-121">In the **Feature management** workspace, in the list of available features, search for and select **Shop similar description**.</span></span>
1. <span data-ttu-id="de94b-122">Aktivieren Sie im rechten Bereich **Aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="de94b-122">In the right pane, select **Enable**.</span></span>

> [!NOTE]
> <span data-ttu-id="de94b-123">Wenn Sie die Funktion aktivieren, beginnt das System mit dem Generieren von Produktempfehlungslisten.</span><span class="sxs-lookup"><span data-stu-id="de94b-123">When you turn on the feature, the system starts to generate product recommendation lists.</span></span> <span data-ttu-id="de94b-124">Es kann bis zu einem Tag dauern, bis diese Listen online und an den POS-Terminals verfügbar und sichtbar sind.</span><span class="sxs-lookup"><span data-stu-id="de94b-124">It might take up to a day for those lists to become available and visible online and on POS terminals.</span></span>
>
> <span data-ttu-id="de94b-125">Wenn Sie die Funktion deaktivieren, sind andere Typen von Produktempfehlungen nicht betroffen.</span><span class="sxs-lookup"><span data-stu-id="de94b-125">If you turn off the feature, other types of product recommendations aren't affected.</span></span> <span data-ttu-id="de94b-126">Weitere Informationen zu Produktempfehlungen finden Sie unter [Überblick über Produktempfehlungen](product-recommendations.md).</span><span class="sxs-lookup"><span data-stu-id="de94b-126">For more information about product recommendations, see [Product recommendations overview](product-recommendations.md).</span></span>

## <a name="add-a-shop-similar-description-button-to-product-details-pages"></a><span data-ttu-id="de94b-127">Den Produktdetailseiten eine „Produkte mit ähnlicher Beschreibung kaufen“-Schaltfläche hinzufügen</span><span class="sxs-lookup"><span data-stu-id="de94b-127">Add a Shop similar description button to product details pages</span></span>

<span data-ttu-id="de94b-128">Nachdem Sie die Empfehlungsfunktion „Produkte mit ähnlicher Beschreibung kaufen“ in der Commerce-Zentralverwaltung aktiviert haben, können Sie dem Kauffeld einer beliebigen Produktdetailseite (PDP) eine **Produkte mit ähnlicher Beschreibung kaufen**-Schaltfläche hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="de94b-128">After you turn on the "shop similar description" recommendations feature in Commerce headquarters, you can add a **Shop similar description** button to the buy box on any product details page (PDP).</span></span> <span data-ttu-id="de94b-129">Ein Kunde, der diese Schaltfläche auswählt, wird zu einer speziellen **Produkte mit ähnlicher Beschreibung kaufen**-Seite weitergeleitet, auf der visuell ähnliche Produkte angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="de94b-129">A customer who selects this button is taken to a dedicated **Shop similar description** page that shows visually similar products.</span></span> <span data-ttu-id="de94b-130">Anschließend kann der Kunde Auswahlen verwenden, um die Produkte weiter zu filtern.</span><span class="sxs-lookup"><span data-stu-id="de94b-130">The customer can then use selectors to further filter the products.</span></span>

<span data-ttu-id="de94b-131">Gehen Sie folgendermaßen vor, um einer PDP eine **Produkte mit ähnlicher Beschreibung kaufen**-Schaltfläche mithilfe des Commerce-Website-Generators hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="de94b-131">To add a **Shop similar description** button to a PDP by using Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="de94b-132">Öffnen Sie eine vorhandene Site Builder-Seite, die ein Kauffeld enthält.</span><span class="sxs-lookup"><span data-stu-id="de94b-132">Open an existing site builder page that contains a buy box module.</span></span>
1. <span data-ttu-id="de94b-133">Wählen Sie im linken Navigationsbereich das Kauffeld aus.</span><span class="sxs-lookup"><span data-stu-id="de94b-133">In the left navigation pane, select the buy box module.</span></span>
1. <span data-ttu-id="de94b-134">Aktivieren Sie im rechten Bereich das Kontrollkästchen **Link für „Produkte mit ähnlicher Beschreibung kaufen“ aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="de94b-134">In the right pane, select the **Enable Shop Similar description Link** check box.</span></span>
1. <span data-ttu-id="de94b-135">Wählen Sie **Speichern** aus.</span><span class="sxs-lookup"><span data-stu-id="de94b-135">Select **Save**.</span></span>
1. <span data-ttu-id="de94b-136">Wählen **Bearbeiten beenden**, um die Seite einzuchecken, und wählen Sie dann **Veröffentlichen**, um sie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="de94b-136">Select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span> <span data-ttu-id="de94b-137">Nach der Veröffentlichung der Seite enthält die PDP eine **Produkte mit ähnlicher Beschreibung kaufen**-Schaltfläche.</span><span class="sxs-lookup"><span data-stu-id="de94b-137">After the page is published, the PDP will include a **Shop similar description** button.</span></span>

<span data-ttu-id="de94b-138">Die folgende Abbildung zeigt das Kontrollkästchen **Link für „Produkte mit ähnlicher Beschreibung kaufen“ aktivieren**-Schaltfläche und die **Produkte mit ähnlicher Beschreibung kaufen**-Schaltfläche auf einer Beispiel-PDP im Site Builder.</span><span class="sxs-lookup"><span data-stu-id="de94b-138">The following illustration shows the **Enable shop similar description Link** check box and the **Shop similar description** button on an example PDP in site builder.</span></span>

![Das Kontrollkästchen „Link für Produkte mit ähnlicher Beschreibung kaufen“ und die Schaltfläche „Produkte mit ähnlicher Beschreibung kaufen“ auf einer Beispiel-PDP im Site Builder aktivieren](./media/ter_site_builder_buybox_button.png)

## <a name="additional-resources"></a><span data-ttu-id="de94b-140">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="de94b-140">Additional resources</span></span>

[<span data-ttu-id="de94b-141">Überblick über Produktempfehlungen</span><span class="sxs-lookup"><span data-stu-id="de94b-141">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="de94b-142">Aktivieren von Azure Data Lake Storage in einer Dynamics 365 Commerce Umgebung</span><span class="sxs-lookup"><span data-stu-id="de94b-142">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="de94b-143">Produktempfehlungen aktivieren</span><span class="sxs-lookup"><span data-stu-id="de94b-143">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="de94b-144">Link „Ähnliche Outfits kaufen“ aktivieren</span><span class="sxs-lookup"><span data-stu-id="de94b-144">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="de94b-145">Anpassung der Ergebnisse der AI-ML-Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="de94b-145">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="de94b-146">Manuell kuratierte Empfehlungen erstellen</span><span class="sxs-lookup"><span data-stu-id="de94b-146">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="de94b-147">Produktempfehlungs-FAQs</span><span class="sxs-lookup"><span data-stu-id="de94b-147">Product recommendations FAQ</span></span>](faq-recommendations.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]