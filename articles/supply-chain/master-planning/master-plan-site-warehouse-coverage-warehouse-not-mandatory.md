---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch
description: In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist nicht obligatorisch.
author: roxanadiaconu
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8350646e70c7ea7d705a69ecb52f389e829a0fc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5833472"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="cdd59-104">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="cdd59-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cdd59-105">In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird.</span><span class="sxs-lookup"><span data-stu-id="cdd59-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="cdd59-106">Die Lagerortdimension ist nicht obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="cdd59-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="cdd59-107">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="cdd59-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="cdd59-108">Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="cdd59-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="cdd59-109">Diese Einstellung kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="cdd59-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="cdd59-110">Die Lagerortdimension ist nicht auf obligatorisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdd59-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="cdd59-111">Der Lagerort ist unter Umständen bekannt, wird jedoch nicht in der Produktprogrammplanberechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="cdd59-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="cdd59-112">Die Standort- und Lagerortdimension werden für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdd59-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="cdd59-113">Für die Disposition können auch andere Dimensionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="cdd59-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="cdd59-114">Für diese ergeben sich jedoch keinerlei Auswirkungen durch die Funktion für mehrere Standorte.</span><span class="sxs-lookup"><span data-stu-id="cdd59-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="cdd59-115">In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cdd59-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="cdd59-116">Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:</span><span class="sxs-lookup"><span data-stu-id="cdd59-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="cdd59-117">Der Lagerort ist auf Manuell festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdd59-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="cdd59-118">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="cdd59-119">Wählen Sie auf dem Inforegister **Produktprogrammplanung** das Feld **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="cdd59-120">Für den Artikel ist die Artikeldeckung definiert.</span><span class="sxs-lookup"><span data-stu-id="cdd59-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="cdd59-121">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="cdd59-122">Wählen Sie einen Artikel aus, und klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Plan** auf **Artikeldeckung**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-122">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="cdd59-123">Für den Lagerort sind Auffüllbeziehungen definiert.</span><span class="sxs-lookup"><span data-stu-id="cdd59-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="cdd59-124">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="cdd59-125">Wählen Sie auf dem Inforegister **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="cdd59-126">Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt.</span><span class="sxs-lookup"><span data-stu-id="cdd59-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="cdd59-127">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="cdd59-128">Wählen Sie einen Artikel aus, und klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Plan** auf **Standardauftragseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-128">Select the item, and then, on the Action Pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="cdd59-129">Im Formular **Standardauftragseinstellungen** sehen Sie den **Standardauftragstyp**.</span><span class="sxs-lookup"><span data-stu-id="cdd59-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Bedarf an Standort und Lagerort, Lagerort nicht obligatorisch](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="cdd59-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cdd59-131">Additional resources</span></span>
--------

[<span data-ttu-id="cdd59-132">Hauptpläne und Funktion für mehrere Standorte – Übersicht</span><span class="sxs-lookup"><span data-stu-id="cdd59-132">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="cdd59-133">Hauptplanung für Standortdeckung, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="cdd59-133">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="cdd59-134">Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="cdd59-134">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="cdd59-135">Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="cdd59-135">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="cdd59-136">Die Stücklistenversion bestimmen</span><span class="sxs-lookup"><span data-stu-id="cdd59-136">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]