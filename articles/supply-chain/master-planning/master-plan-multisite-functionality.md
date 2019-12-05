---
title: Überblick über die Masterplanung und die standortübergreifende Funktionalität
description: Der Produktprogrammplan berücksichtigt die Einstellungen der Site Lagerortlagerdimensionen.
author: roxanadiaconu
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventLocation, InventSite
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2434
ms.assetid: 7f05c031-a446-4168-8cce-03a6305f5c4d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0b715e0c17263519a9bb1b3780170812271d93d
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813752"
---
# <a name="master-planning-and-multisite-functionality-overview"></a><span data-ttu-id="dce58-103">Überblick über die Masterplanung und die standortübergreifende Funktionalität</span><span class="sxs-lookup"><span data-stu-id="dce58-103">Master planning and multisite functionality overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dce58-104">Der Produktprogrammplan berücksichtigt die Einstellungen der Site Lagerortlagerdimensionen.</span><span class="sxs-lookup"><span data-stu-id="dce58-104">Master planning takes the settings of the site and warehouse inventory dimensions into account.</span></span> 

<span data-ttu-id="dce58-105">Die Standortdimension ist obligatorisch, und Sie können festlegen, dass auch die Lagerortdimension obligatorisch sein soll.</span><span class="sxs-lookup"><span data-stu-id="dce58-105">The site dimension is mandatory, and you can set the warehouse dimension to be mandatory.</span></span>

<span data-ttu-id="dce58-106">Wenn eine Dimension obligatorisch ist, muss bei allen Lagerbuchungen ein Dimensionswert eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="dce58-106">When a dimension is mandatory, a dimension value must be entered on all inventory transactions.</span></span> <span data-ttu-id="dce58-107">Daher sind bei der Produktprogrammplanung der Standort und der Lagerort für den Anfangsbedarf bekannt.</span><span class="sxs-lookup"><span data-stu-id="dce58-107">Therefore, during master planning, the site and the warehouse for the initial demand are known.</span></span> <span data-ttu-id="dce58-108">Die Standortdimension ist auch konsistent, sodass sich der Standortwert während der Auflösung des Bedarfs auf niedrigerer Ebene nicht ändert.</span><span class="sxs-lookup"><span data-stu-id="dce58-108">The site dimension is also consistent so that during the explosion of lower-level demand, the site value does not change.</span></span>

<span data-ttu-id="dce58-109">Wenn der Lagerort nicht auf obligatorisch festgelegt ist, ist er möglicherweise nicht aus dem Anfangsbedarf bekannt.</span><span class="sxs-lookup"><span data-stu-id="dce58-109">When the warehouse is not set to mandatory, it may not be known from the initial demand.</span></span> <span data-ttu-id="dce58-110">Das Planungsmodul muss den zu verwendenden Lagerort auf Grundlage der für den Artikel festgelegten Einstellungen, einzelner Lagerorte und der Details der Auftragsposition bestimmen.</span><span class="sxs-lookup"><span data-stu-id="dce58-110">The planning engine must determine which warehouse to use based on the settings that are defined for the item, individual warehouses, and the details of the order line.</span></span>

<span data-ttu-id="dce58-111">In den folgenden Themen wird die Funktionsweise des Planungsmoduls bei Definition unterschiedlicher Einstellungen zur Bestimmung des zu verwendenden Lagerorts erläutert.</span><span class="sxs-lookup"><span data-stu-id="dce58-111">The following topics describe how the planning engine works, when different settings are defined, to determine the warehouse to use.</span></span>

[<span data-ttu-id="dce58-112">Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="dce58-112">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="dce58-113">Hauptplanung für Standortdeckung, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="dce58-113">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="dce58-114">Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="dce58-114">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="dce58-115">Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="dce58-115">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="dce58-116">Die Stücklistenversion bestimmen</span><span class="sxs-lookup"><span data-stu-id="dce58-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



