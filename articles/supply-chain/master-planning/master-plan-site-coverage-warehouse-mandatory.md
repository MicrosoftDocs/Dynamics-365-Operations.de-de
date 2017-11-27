---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch
description: In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist eine zwingende Dimension.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 2454
ms.assetid: aa135030-f98c-48bf-902c-e52f680dc247
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ca01913a0338004fabcda5136108ec3c5be8ff7
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="master-planning-for-site-coverage-mandatory-warehouse"></a><span data-ttu-id="61965-104">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="61965-104">Master planning for site coverage, mandatory warehouse</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="61965-105">In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird.</span><span class="sxs-lookup"><span data-stu-id="61965-105">This topic describes how an item that has the site as coverage dimension is planned.</span></span> <span data-ttu-id="61965-106">Die Lagerortdimension ist eine zwingende Dimension.</span><span class="sxs-lookup"><span data-stu-id="61965-106">Warehouse is a mandatory dimension.</span></span>

<span data-ttu-id="61965-107">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="61965-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="61965-108">Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61965-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="61965-109">Diese Einstellung kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="61965-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="61965-110">Die Lagerortdimension ist als obligatorische Dimension festgelegt und muss zwingend für die Bedarfsbuchung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="61965-110">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="61965-111">Die Standortdimension ist für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61965-111">The site dimension is set for coverage planning.</span></span> <span data-ttu-id="61965-112">Für die Disposition können auch andere Dimensionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="61965-112">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="61965-113">Für diese ergeben sich jedoch keinerlei Auswirkungen durch die Funktion für mehrere Standorte.</span><span class="sxs-lookup"><span data-stu-id="61965-113">However, they are not affected by the multisite functionality.</span></span>
-   <span data-ttu-id="61965-114">Die Lagerortdimension ist nicht für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61965-114">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="61965-115">Deshalb werden Angebot und Nachfrage nach Standort und möglicherweise auch nach weiteren Dispositionsdimensionen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="61965-115">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="61965-116">In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="61965-116">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="61965-117">Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:</span><span class="sxs-lookup"><span data-stu-id="61965-117">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="61965-118">Für den Artikel ist die Artikeldeckung definiert.</span><span class="sxs-lookup"><span data-stu-id="61965-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="61965-119">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="61965-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="61965-120">Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Artikeldeckung**.</span><span class="sxs-lookup"><span data-stu-id="61965-120">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="61965-121">Für den Lagerort sind Auffüllbeziehungen definiert.</span><span class="sxs-lookup"><span data-stu-id="61965-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="61965-122">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="61965-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="61965-123">Wählen Sie auf der Registerkarte **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.</span><span class="sxs-lookup"><span data-stu-id="61965-123">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="61965-124">Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt.</span><span class="sxs-lookup"><span data-stu-id="61965-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="61965-125">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="61965-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="61965-126">Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Standardauftragseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="61965-126">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="61965-127">Im Formular **Standardauftragseinstellungen** sehen Sie den **Standardauftragstyp**.</span><span class="sxs-lookup"><span data-stu-id="61965-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Bedarf für Disposition an Standort, Lagerort obligatorisch](./media/multisitedemandexplosionscenarioforsitecoveragewarehousemandatory.jpg)



<a name="see-also"></a><span data-ttu-id="61965-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61965-129">See also</span></span>
--------

[<span data-ttu-id="61965-130">Produktprogrammplanung und Funktion für mehrere Standorte</span><span class="sxs-lookup"><span data-stu-id="61965-130">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="61965-131">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="61965-131">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="61965-132">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="61965-132">Master planning - site coverage. warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="61965-133">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="61965-133">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="61965-134">Produktprogrammplanungslauf - Ermittlung der Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="61965-134">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




