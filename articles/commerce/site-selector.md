---
title: Siteauswahlmodul
description: Dieses Thema enthält das Siteauswahlmodul und es wird beschrieben, wie Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: bd54695f54b501631f916328c05bfd47e538d50d
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055829"
---
# <a name="site-selector-module"></a><span data-ttu-id="f4855-103">Siteauswahlmodul</span><span class="sxs-lookup"><span data-stu-id="f4855-103">Site selector module</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="f4855-104">Dieses Thema enthält das Siteauswahlmodul und es wird beschrieben, wie Siteseiten in Microsoft Dynamics 365 Commerce hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f4855-104">This topic covers the site selector module and describes how to add it to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="f4855-105">Übersicht</span><span class="sxs-lookup"><span data-stu-id="f4855-105">Overview</span></span>

<span data-ttu-id="f4855-106">Wenn ein Unternehmen unterschiedliche Websites in verschiedenen Märkten, Regionen und Gebiete hat, benötigen Websitebenutzer eine einfache Möglichkeit, zwischen Websites zu wechseln und ihre bevorzugte Einkaufsseite auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="f4855-106">When a business has different sites across markets, regions, and locales, site users need an easy way to switch between sites and select their preferred shopping site.</span></span> <span data-ttu-id="f4855-107">Um diesem Szenario gerecht zu werden, können Benutzer mit dem Site-Auswahlmodul mehrere Sites durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="f4855-107">To accommodate this scenario, the site selector module lets users browse across multiple sites.</span></span>

<span data-ttu-id="f4855-108">Das Site-Auswahlmodul muss mit der Liste der Sites (Märkte, Regionen oder Gebietsschemas) konfiguriert sein, die Site-Benutzer durchsuchen können.</span><span class="sxs-lookup"><span data-stu-id="f4855-108">The site selector module must be configured with the list of sites (markets, regions, or locales) that site users can browse.</span></span>

> [!NOTE]
> <span data-ttu-id="f4855-109">Das Siteauswahl-Modul ist in Dynamics 365 Commerce 10.0.14 Release verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f4855-109">The site selector module is available in the Dynamics 365 Commerce 10.0.14 release.</span></span>

<span data-ttu-id="f4855-110">Die folgende Abbildung zeigt ein Beispiel für ein Site-Auswahlmodul, das in der Kopfzeile einer Site-Seite enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f4855-110">The following illustration shows an example of a site selector module that is featured in the header of a site page.</span></span>

![Beispiel eines Site-Auswahlmoduls in der Kopfzeile einer Site-Seite](./media/ecommerce-sitepicker.PNG)

## <a name="site-selector-module-properties"></a><span data-ttu-id="f4855-112">Eigenschaften des Siteauswahlmoduls</span><span class="sxs-lookup"><span data-stu-id="f4855-112">Site selector module properties</span></span>

| <span data-ttu-id="f4855-113">Eigenschaftenname</span><span class="sxs-lookup"><span data-stu-id="f4855-113">Property name</span></span> | <span data-ttu-id="f4855-114">Wert</span><span class="sxs-lookup"><span data-stu-id="f4855-114">Value</span></span>                 | <span data-ttu-id="f4855-115">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f4855-115">Description</span></span> |
|---------------|-----------------------|-------------|
| <span data-ttu-id="f4855-116">Überschrift</span><span class="sxs-lookup"><span data-stu-id="f4855-116">Heading</span></span>       | <span data-ttu-id="f4855-117">Text</span><span class="sxs-lookup"><span data-stu-id="f4855-117">Text</span></span>                  | <span data-ttu-id="f4855-118">Die Überschrift für das Modul.</span><span class="sxs-lookup"><span data-stu-id="f4855-118">The heading for the module.</span></span> |
| <span data-ttu-id="f4855-119">Websiteoptionen</span><span class="sxs-lookup"><span data-stu-id="f4855-119">Site options</span></span>  | <span data-ttu-id="f4855-120">Name, Bild, URL</span><span class="sxs-lookup"><span data-stu-id="f4855-120">Name, Image, URL</span></span>      | <span data-ttu-id="f4855-121">Diese Eigenschaft gibt einen Namen, einen Link zur Homepage der Site und ein optionales Bild für jede Site an, die im Modul enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f4855-121">This property specifies a name, a link to the site's home page, and an optional image to show for each site that is included in the module.</span></span> <span data-ttu-id="f4855-122">Das Bild kann eine Flagge oder eine Darstellung eines Marktes, einer Region oder eines Gebietsschemas sein.</span><span class="sxs-lookup"><span data-stu-id="f4855-122">The image can be a flag, or some representation of a market, region, or locale.</span></span> |

## <a name="add-a-site-selector-module-to-a-page"></a><span data-ttu-id="f4855-123">Hinzufügen eines Siteauswahlmoduls zu einer Seite</span><span class="sxs-lookup"><span data-stu-id="f4855-123">Add a site selector module to a page</span></span>

<span data-ttu-id="f4855-124">Das Site-Auswahlmodul kann dem [Header-Modul](author-header-module.md) unter dem Site-Auswahl-Slot hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="f4855-124">The site selector module can be added to the [Header module](author-header-module.md) under the site selector slot.</span></span> <span data-ttu-id="f4855-125">Nach dem Hinzufügen können Sie die Modulüberschrift und die Site-Optionen definieren.</span><span class="sxs-lookup"><span data-stu-id="f4855-125">After it's added, you can define the module heading and site options.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f4855-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f4855-126">Additional resources</span></span>

[<span data-ttu-id="f4855-127">Informationen zur Modulbibliothek</span><span class="sxs-lookup"><span data-stu-id="f4855-127">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="f4855-128">Kopfzeilenmodul</span><span class="sxs-lookup"><span data-stu-id="f4855-128">Header module</span></span>](author-header-module.md)

[<span data-ttu-id="f4855-129">Breadcrumb-Modul</span><span class="sxs-lookup"><span data-stu-id="f4855-129">Breadcrumb module</span></span>](add-breadcrumb.md)

[<span data-ttu-id="f4855-130">Navigationsmenümodul</span><span class="sxs-lookup"><span data-stu-id="f4855-130">Navigation menu module</span></span>](nav-menu-module.md)
