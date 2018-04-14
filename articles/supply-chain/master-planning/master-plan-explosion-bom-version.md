---
title: "Auflösung einer Stücklistenversion"
description: "In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bce6ffd0ee284f2a5e5b5fef0bdfa92e192b2f42
ms.contentlocale: de-de
ms.lasthandoff: 04/13/2018

---

# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="4f5ad-103">Auflösung einer Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="4f5ad-103">Explosion of a BOM version</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="4f5ad-104">In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft.</span><span class="sxs-lookup"><span data-stu-id="4f5ad-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="4f5ad-105">Eine Bedarfsauflösung einer Stücklistenversion erstellt einen Bedarf für jeden Stücklistenpositionsartikel an einem bestimmten Standort (und ggf. in einem bestimmten Lager).</span><span class="sxs-lookup"><span data-stu-id="4f5ad-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="4f5ad-106">In einer standortspezifischen Stückliste kann ein bestimmtes Lager für jede Stücklistenposition definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4f5ad-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="4f5ad-107">Zudem bestimmen die Dimensionseinstellungen des Artikels für jede Stücklistenposition, ob das Lager erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4f5ad-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="4f5ad-108">Der resultierende Bedarf für jeden Stücklistenpositionsartikel wird dann Ausgangspunkt für weitere Bedarfsauflösungen.</span><span class="sxs-lookup"><span data-stu-id="4f5ad-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="4f5ad-109">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="4f5ad-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="4f5ad-110">Die Standortdimension ist obligatorisch und muss in die Bedarfsbuchung eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4f5ad-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="4f5ad-111">Die Standortdimension ist einheitlich.</span><span class="sxs-lookup"><span data-stu-id="4f5ad-111">The site dimension is consistent.</span></span> <span data-ttu-id="4f5ad-112">Aus diesem Grund handelt es sich bei dem Standort für geringen Bedarf um den Standort, der auch in der anfänglichen Bedarfsbuchung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4f5ad-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="4f5ad-113">In der folgenden Illustration ist der Ablauf der Bedarfsauflösung für die Produktprogrammplanung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4f5ad-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Bedarfsauflösung – Verwenden einer Stücklistenversion](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="see-also"></a><span data-ttu-id="4f5ad-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f5ad-115">See also</span></span>
--------

[<span data-ttu-id="4f5ad-116">Produktprogrammplanungslauf - Ermittlung der Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="4f5ad-116">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="4f5ad-117">Produktprogrammplanung und Funktion für mehrere Standorte</span><span class="sxs-lookup"><span data-stu-id="4f5ad-117">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)




