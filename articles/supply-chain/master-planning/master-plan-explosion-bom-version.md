---
title: Auflösung einer Stücklistenversion
description: In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 367b662a43b3c3255632f20aeb821b973b04d890
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833592"
---
# <a name="explosion-of-a-bom-version"></a><span data-ttu-id="3b454-103">Auflösung einer Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="3b454-103">Explosion of a BOM version</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3b454-104">In diesem Artikel wird beschrieben ein, das Produktprogrammplanungsszenario Auflösung einer Stückliste (BOM)- Version betrifft.</span><span class="sxs-lookup"><span data-stu-id="3b454-104">This article explains a master planning scenario that involves explosion of a bill of materials (BOM) version.</span></span>

<span data-ttu-id="3b454-105">Eine Bedarfsauflösung einer Stücklistenversion erstellt einen Bedarf für jeden Stücklistenpositionsartikel an einem bestimmten Standort (und ggf. in einem bestimmten Lager).</span><span class="sxs-lookup"><span data-stu-id="3b454-105">A demand explosion of a bill of materials (BOM) version creates a demand for each BOM line item at a specific site and, possibly, at a specific warehouse.</span></span> <span data-ttu-id="3b454-106">In einer standortspezifischen Stückliste kann ein bestimmtes Lager für jede Stücklistenposition definiert werden.</span><span class="sxs-lookup"><span data-stu-id="3b454-106">In a site-specific BOM, a specific warehouse can be defined for each BOM line.</span></span> <span data-ttu-id="3b454-107">Zudem bestimmen die Dimensionseinstellungen des Artikels für jede Stücklistenposition, ob das Lager erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3b454-107">Additionally, for each BOM line, the item's dimension settings determine whether the warehouse is required.</span></span> <span data-ttu-id="3b454-108">Der resultierende Bedarf für jeden Stücklistenpositionsartikel wird dann Ausgangspunkt für weitere Bedarfsauflösungen.</span><span class="sxs-lookup"><span data-stu-id="3b454-108">The resulting demand for each BOM line item then becomes the starting point for additional demand explosion.</span></span> <span data-ttu-id="3b454-109">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="3b454-109">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="3b454-110">Die Standortdimension ist obligatorisch und muss in die Bedarfsbuchung eingegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3b454-110">The site dimension is mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="3b454-111">Die Standortdimension ist einheitlich.</span><span class="sxs-lookup"><span data-stu-id="3b454-111">The site dimension is consistent.</span></span> <span data-ttu-id="3b454-112">Aus diesem Grund handelt es sich bei dem Standort für geringen Bedarf um den Standort, der auch in der anfänglichen Bedarfsbuchung enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3b454-112">Therefore, the site for lower-level demand is the same as the site on the initial demand transaction.</span></span>

<span data-ttu-id="3b454-113">In der folgenden Illustration ist der Ablauf der Bedarfsauflösung für die Produktprogrammplanung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3b454-113">The following illustration shows how the process for master planning demand explosion.</span></span> ![Bedarfsauflösung – Verwenden einer Stücklistenversion](./media/multisitedemandexplosionscenariousingbomversion.gif)

<a name="additional-resources"></a><span data-ttu-id="3b454-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3b454-115">Additional resources</span></span>
--------

[<span data-ttu-id="3b454-116">Die Stücklistenversion bestimmen</span><span class="sxs-lookup"><span data-stu-id="3b454-116">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)

[<span data-ttu-id="3b454-117">Hauptpläne und Funktion für mehrere Standorte – Übersicht</span><span class="sxs-lookup"><span data-stu-id="3b454-117">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]