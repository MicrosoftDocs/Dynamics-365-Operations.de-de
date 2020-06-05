---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch
description: In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist obligatorisch.
author: roxanadiaconu
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2554
ms.assetid: 3211e95f-b91a-4d27-8d92-f328ae2bcf12
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a07a4588d042af53d6281afc174ff58ecf24ca06
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383342"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-mandatory"></a><span data-ttu-id="5022d-104">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="5022d-104">Master planning for site and warehouse coverage, warehouse mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5022d-105">In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird.</span><span class="sxs-lookup"><span data-stu-id="5022d-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="5022d-106">Die Lagerortdimension ist obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="5022d-106">The warehouse dimension is mandatory.</span></span>

<span data-ttu-id="5022d-107">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="5022d-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="5022d-108">Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5022d-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="5022d-109">Die Lagerortdimension ist als obligatorische Dimension festgelegt und muss zwingend für die Bedarfsbuchung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5022d-109">The warehouse dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="5022d-110">Die Standort- und Lagerortdimension werden für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5022d-110">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="5022d-111">Für die Disposition können auch andere Dimensionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5022d-111">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="5022d-112">Für diese ergeben sich jedoch keinerlei Auswirkungen durch die Funktion für mehrere Standorte.</span><span class="sxs-lookup"><span data-stu-id="5022d-112">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="5022d-113">In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5022d-113">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="5022d-114">Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:</span><span class="sxs-lookup"><span data-stu-id="5022d-114">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="5022d-115">Der Lagerort ist auf **Manuell** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5022d-115">The warehouse is set to **Manual**.</span></span> <span data-ttu-id="5022d-116">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="5022d-116">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5022d-117">Wählen Sie auf dem Inforegister **Produktprogrammplanung** das Feld **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="5022d-117">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="5022d-118">Für den Artikel ist die Artikeldeckung definiert.</span><span class="sxs-lookup"><span data-stu-id="5022d-118">Item coverage is defined for the item.</span></span> <span data-ttu-id="5022d-119">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="5022d-119">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5022d-120">Wählen Sie einen Artikel aus, und klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Plan** auf **Artikeldeckung**.</span><span class="sxs-lookup"><span data-stu-id="5022d-120">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="5022d-121">Für den Lagerort sind Auffüllbeziehungen definiert.</span><span class="sxs-lookup"><span data-stu-id="5022d-121">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="5022d-122">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="5022d-122">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5022d-123">Wählen Sie auf dem Inforegister **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.</span><span class="sxs-lookup"><span data-stu-id="5022d-123">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="5022d-124">Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5022d-124">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="5022d-125">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="5022d-125">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5022d-126">Wählen Sie einen Artikel aus, und klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Plan** auf **Standardauftragseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="5022d-126">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="5022d-127">Im Formular **Standardauftragseinstellungen** sehen Sie den **Standardauftragstyp**.</span><span class="sxs-lookup"><span data-stu-id="5022d-127">In the **Default order settings** form, see the **Default order type**.</span></span>

![Disposition an Bedarfsstandort und Lagerort, Lagerort obligatorisch](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousemandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="5022d-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5022d-129">Additional resources</span></span>
--------

[<span data-ttu-id="5022d-130">Hauptpläne und Funktion für mehrere Standorte – Übersicht</span><span class="sxs-lookup"><span data-stu-id="5022d-130">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="5022d-131">Hauptplanung für Standortdeckung, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="5022d-131">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5022d-132">Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="5022d-132">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="5022d-133">Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="5022d-133">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="5022d-134">Die Stücklistenversion bestimmen</span><span class="sxs-lookup"><span data-stu-id="5022d-134">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



