---
title: Auflösung einer Stücklistenversion
description: In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransExplosion
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19211
ms.assetid: fe08c2e6-9cc5-4e34-bbb2-cd07843403b5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 617d9c3f05f2db30ec075a07b54c4827e668c20e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220847"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="4fdaa-103">Auflösung einer Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="4fdaa-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fdaa-104">In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft.</span><span class="sxs-lookup"><span data-stu-id="4fdaa-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="4fdaa-105">Eine Bedarfsauflösung einer Stücklistenversion erstellt einen Bedarf für jeden Stücklistenpositionsartikel an einem bestimmten Standort (und ggf. in einem bestimmten Lager).</span><span class="sxs-lookup"><span data-stu-id="4fdaa-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="4fdaa-106">In einer standortspezifischen Stückliste kann ein bestimmtes Lager für jede Stücklistenposition definiert werden.</span><span class="sxs-lookup"><span data-stu-id="4fdaa-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="4fdaa-107">Zudem bestimmen die Dimensionseinstellungen des Artikels für jede Stücklistenposition, ob das Lager erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4fdaa-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="4fdaa-108">Der resultierende Bedarf für jeden Stücklistenpositionsartikel wird dann Ausgangspunkt für weitere Bedarfsauflösungen.</span><span class="sxs-lookup"><span data-stu-id="4fdaa-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="4fdaa-109">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="4fdaa-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="4fdaa-110">Die Standortdimension ist obligatorisch und muss in die Bedarfsbuchung eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="4fdaa-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="4fdaa-111">Die Standortdimension ist einheitlich.</span><span class="sxs-lookup"><span data-stu-id="4fdaa-111">The site dimension is consistent.</span></span> <span data-ttu-id="4fdaa-112">Aus diesem Grund handelt es sich bei dem Standort für geringen Bedarf um den Standort, der auch in der anfänglichen Bedarfsbuchung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="4fdaa-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="4fdaa-113">In der folgenden Illustration ist der Ablauf der Bedarfsauflösung für die Produktprogrammplanung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4fdaa-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Bedarfsauflösung – Verwenden einer Stücklistenversion](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="4fdaa-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4fdaa-115">Additional resources</span></span>
--------

[<span data-ttu-id="4fdaa-116">Die Stücklistenversion bestimmen</span><span class="sxs-lookup"><span data-stu-id="4fdaa-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="4fdaa-117">Hauptpläne und Funktion für mehrere Standorte – Übersicht</span><span class="sxs-lookup"><span data-stu-id="4fdaa-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]