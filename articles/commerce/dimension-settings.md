---
title: Wenden Sie Anzeigeeinstellungen für Produktabmessungen an
description: In diesem Thema werden die Anzeigeeinstellungen für Produktabmessungen behandelt und deren Anwendung in Microsoft Dynamics 365 Commerce beschrieben.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117225"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="28570-103">Wenden Sie Anzeigeeinstellungen für Produktabmessungen an</span><span class="sxs-lookup"><span data-stu-id="28570-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="28570-104">In diesem Thema werden die Anzeigeeinstellungen für Produktabmessungen behandelt und deren Anwendung in Microsoft Dynamics 365 Commerce beschrieben.</span><span class="sxs-lookup"><span data-stu-id="28570-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="28570-105">Dynamics 365 Commerce unterstützt die Verwendung von Größe, Stil und Farbabmessungen um Produktvarianten zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="28570-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="28570-106">Bemaßungen werden normalerweise als Textwerte angezeigt, z. B. Klein, Mittel und Groß für Größen und Schwarz und Braun für Farben.</span><span class="sxs-lookup"><span data-stu-id="28570-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="28570-107">Wenn ein Produkt jedoch viele Variationen unterstützt, kann es schwierig sein, in Produktvarianten zu suchen, weil mehrere Auswahlen erforderlich sind, um das Bild für jede Produktvariante anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="28570-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="28570-108">Um das Durchsuchen von Produktvarianten zu vereinfachen, kann die Version 10.0.20 von Commerce Bilder und hexadezimalen (hexadezimale) Codes verwenden, um Abmessungen als Farbfelder anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="28570-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="28570-109">Im Commerce Website-Generator werden Abmessungsinstellungen unter **Seiteneinstellungen \> Erweiterungen \> Abmessungsverwaltung** definiert.</span><span class="sxs-lookup"><span data-stu-id="28570-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="28570-110">Die folgende Abbildung zeigt ein Beispiel für die Abmessungseinstellungen im Website-Generator.</span><span class="sxs-lookup"><span data-stu-id="28570-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Beispiel für Website-Einstellungen im Commerce Website-Generator](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="28570-112">Es stehen zwei Abmessungseinstellungen zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="28570-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="28570-113">**Abmessungen, die als Bild angezeigt werden sollen** – Geben Sie an, welche Ambessungen auf E-Commerce-Websiteseiten als Farbfelder angezeigt werden sollen, z. B. auf Produktdetailseiten (PDPs) und Seiten mit Suchergebnislisten.</span><span class="sxs-lookup"><span data-stu-id="28570-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="28570-114">Jede Kombination aus Farbe, Größe und Stilabmessungen kann als Farbfeld angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="28570-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="28570-115">Wenn eine Abmessung für die Anzeige als Farbfeld ausgewählt ist, sucht das Commerce Modul Rendering nach einer verfügbaren Konfiguration eines Hexadezimalcode-Farbfelds.</span><span class="sxs-lookup"><span data-stu-id="28570-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="28570-116">Wenn kein Hexadezimalcode konfiguriert ist, sucht die Systemlogik nach einer Konfiguration eines Bild-URL-Farbfelds.</span><span class="sxs-lookup"><span data-stu-id="28570-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="28570-117">Wenn weder ein Hexadezimalcode noch eine Bild-URL konfiguriert sind, wird Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28570-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="28570-118">Die folgende Abbildung zeigt ein Beispiel, in dem ein PDP als E-Commerce Site einschließlich Farb- und Größenfelder angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="28570-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="28570-119">In diesem Beispiel wird ein Hexadezimalcode für die Farbdimension konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="28570-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="28570-120">Daher werden Farbfelder als Farben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28570-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="28570-121">Für die Größenabmessung ist jedoch weder ein Hexadezimalcode noch eine Bild-URL konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="28570-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="28570-122">Daher wird Text angezeigt.</span><span class="sxs-lookup"><span data-stu-id="28570-122">Therefore, text is shown.</span></span>

    ![Beispiel für die Farbabmessung, die auf einer E-Commerce-Produktdetailseite als Farbfelder angezeigt wird](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="28570-124">**Abmessungen, die auf der Produktkarte angezeigt werden sollen** – Geben Sie an, welche Abmessungen auf Produktkarten angezeigt werden sollen, die in Listen und auf Listenseiten angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="28570-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="28570-125">Bevor eine Abmessung auf einer Produktkarte angezeigt werden kann, muss diese Einstellung für diese Abmessung aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="28570-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="28570-126">Die Einstellung **Abmessungen, die als Bild angezeigt werden sollen** sollte auch aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="28570-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="28570-127">Das Farbfeldauswahlverhalten auf Produktkarten ist für die Farbabmessung optimiert.</span><span class="sxs-lookup"><span data-stu-id="28570-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="28570-128">Für andere Dimensionen ist möglicherweise eine Ansichtserweiterung erforderlich, um das Farbfeldauswahlverhalten anzupassen.</span><span class="sxs-lookup"><span data-stu-id="28570-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="28570-129">Die folgende Abbildung zeigt ein Beispiel, in dem eine Listenseite auf einer E-Commerce-Website Produktkarten mit Farbfeldern enthält.</span><span class="sxs-lookup"><span data-stu-id="28570-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Beispiel für die Farbabmessung, die auf einer E-Commerce-Produktlistenseite als Farbfelder angezeigt wird](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="28570-131">Informationen zum Konfigurieren der Produktabmessungen, sodass sie auf den Websiteseiten als Farbfelder angezeigt werden, finden Sie unter [Konfigurieren Sie Produktdimensionswerte so, dass sie als Farbfelder angezeigt werden](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="28570-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28570-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28570-132">Additional resources</span></span>

[<span data-ttu-id="28570-133">Informationen zur Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="28570-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="28570-134">Suchergebnismodul</span><span class="sxs-lookup"><span data-stu-id="28570-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="28570-135">Kauffeldmodul</span><span class="sxs-lookup"><span data-stu-id="28570-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="28570-136">Konfigurieren Sie Produktdimensionswerte so, dass sie als Farbfelder angezeigt werden</span><span class="sxs-lookup"><span data-stu-id="28570-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
