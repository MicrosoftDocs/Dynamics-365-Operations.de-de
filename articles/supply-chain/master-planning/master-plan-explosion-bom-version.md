---
title: Auflösung einer Stücklistenversion
description: In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dbdfc169365cb73e13383b11efcd8983aef4bbca
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 11/18/2019
ms.locfileid: "2815317"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="11603-103">Auflösung einer Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="11603-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="11603-104">In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft.</span><span class="sxs-lookup"><span data-stu-id="11603-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="11603-105">Eine Bedarfsauflösung einer Stücklistenversion erstellt einen Bedarf für jeden Stücklistenpositionsartikel an einem bestimmten Standort (und ggf. in einem bestimmten Lager).</span><span class="sxs-lookup"><span data-stu-id="11603-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="11603-106">In einer standortspezifischen Stückliste kann ein bestimmtes Lager für jede Stücklistenposition definiert werden.</span><span class="sxs-lookup"><span data-stu-id="11603-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="11603-107">Zudem bestimmen die Dimensionseinstellungen des Artikels für jede Stücklistenposition, ob das Lager erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="11603-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="11603-108">Der resultierende Bedarf für jeden Stücklistenpositionsartikel wird dann Ausgangspunkt für weitere Bedarfsauflösungen.</span><span class="sxs-lookup"><span data-stu-id="11603-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="11603-109">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="11603-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="11603-110">Die Standortdimension ist obligatorisch und muss in die Bedarfsbuchung eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="11603-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="11603-111">Die Standortdimension ist einheitlich.</span><span class="sxs-lookup"><span data-stu-id="11603-111">The site dimension is consistent.</span></span> <span data-ttu-id="11603-112">Aus diesem Grund handelt es sich bei dem Standort für geringen Bedarf um den Standort, der auch in der anfänglichen Bedarfsbuchung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="11603-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="11603-113">In der folgenden Illustration ist der Ablauf der Bedarfsauflösung für die Produktprogrammplanung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="11603-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Bedarfsauflösung – Verwenden einer Stücklistenversion](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="11603-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="11603-115">Additional resources</span></span>
--------

[<span data-ttu-id="11603-116">Die Stücklistenversion bestimmen</span><span class="sxs-lookup"><span data-stu-id="11603-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="11603-117">Hauptpläne und Funktion für mehrere Standorte – Übersicht</span><span class="sxs-lookup"><span data-stu-id="11603-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)



