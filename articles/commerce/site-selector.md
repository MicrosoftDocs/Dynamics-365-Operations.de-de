---
title: Siteauswahlmodul
description: Dieses Thema enthält das Siteauswahlmodul und es wird beschrieben, wie Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
ms.date: 10/20/2020
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
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 6e8eefe7afe385ca77eca6027638ff938e1356e3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791774"
---
# <a name="site-selector-module"></a><span data-ttu-id="a20aa-103">Siteauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="a20aa-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a20aa-104">Dieses Thema enthält das Siteauswahlmodul und es wird beschrieben, wie Websiteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a20aa-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a20aa-105">Wenn ein Unternehmen unterschiedliche Websites in verschiedenen Märkten, Regionen und Gebiete hat, benötigen Websitebenutzer eine einfache Möglichkeit, zwischen Websites zu wechseln und ihre bevorzugte Einkaufsseite auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="a20aa-105">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="a20aa-106">Um diesem Szenario gerecht zu werden, können Benutzer mit dem Site-Auswahlmodul mehrere Sites durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="a20aa-106">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="a20aa-107">Das Site-Auswahlmodul muss mit der Liste der Sites (Märkte, Regionen oder Gebietsschemas) konfiguriert sein, die Site-Benutzer durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="a20aa-107">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="a20aa-108">Das Siteauswahl-Modul ist in Dynamics 365 Commerce 10.0.14 Release verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a20aa-108">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="a20aa-109">Die folgende Abbildung zeigt ein Beispiel für ein Site-Auswahlmodul, das in der Kopfzeile einer Site-Seite enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a20aa-109">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Beispiel eines Site-Auswahlmoduls in der Kopfzeile einer Site-Seite](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="a20aa-111">Eigenschaften des Siteauswahlmoduls</span><span class="sxs-lookup"><span data-stu-id="a20aa-111">Site selector module properties</span></span>

| <span data-ttu-id="a20aa-112">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="a20aa-112">Property name</span></span> | <span data-ttu-id="a20aa-113">Wert</span><span class="sxs-lookup"><span data-stu-id="a20aa-113">Value</span></span>                 | <span data-ttu-id="a20aa-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a20aa-114">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="a20aa-115">Überschrift</span><span class="sxs-lookup"><span data-stu-id="a20aa-115">Heading</span></span>       | <span data-ttu-id="a20aa-116">Text</span><span class="sxs-lookup"><span data-stu-id="a20aa-116">Text</span></span>                  | <span data-ttu-id="a20aa-117">Die Überschrift für das Modul.</span><span class="sxs-lookup"><span data-stu-id="a20aa-117">The heading for the module.</span></span> |
| <span data-ttu-id="a20aa-118">Websiteoptionen</span><span class="sxs-lookup"><span data-stu-id="a20aa-118">Site options</span></span>  | <span data-ttu-id="a20aa-119">Name, Bild, URL</span><span class="sxs-lookup"><span data-stu-id="a20aa-119">Name, Image, URL</span></span>      | <span data-ttu-id="a20aa-120">Diese Eigenschaft gibt einen Namen, einen Link zur Homepage der Site und ein optionales Bild für jede Site an, die im Modul enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="a20aa-120">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="a20aa-121">Das Bild kann eine Flagge oder eine Darstellung eines Marktes, einer Region oder eines Gebietsschemas sein.</span><span class="sxs-lookup"><span data-stu-id="a20aa-121">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="a20aa-122">Hinzufügen eines Siteauswahlmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="a20aa-122">Add a site selector module to a page</span></span>

<span data-ttu-id="a20aa-123">Das Site-Auswahlmodul kann dem [Header-Modul](author-header-module.md) unter dem Site-Auswahl-Slot hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a20aa-123">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="a20aa-124">Nach dem Hinzufügen können Sie die Modulüberschrift und die Site-Optionen definieren.</span><span class="sxs-lookup"><span data-stu-id="a20aa-124">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a20aa-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a20aa-125">Additional resources</span></span>

[<span data-ttu-id="a20aa-126">Informationen zur Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="a20aa-126">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a20aa-127">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="a20aa-127">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="a20aa-128">Breadcrumb-Modul</span><span class="sxs-lookup"><span data-stu-id="a20aa-128">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="a20aa-129">Navigationsmenümodul</span><span class="sxs-lookup"><span data-stu-id="a20aa-129">Navigation menu module</span></span>](nav-menu-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]