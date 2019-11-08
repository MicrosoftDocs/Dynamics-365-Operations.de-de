---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch
description: In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird. Die Lagerortdimension ist nicht obligatorisch.
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResStorageDimensionGroup, ReqItemTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2514
ms.assetid: 92d47bdd-df68-4f60-ac9a-96aa08236c26
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34a1a2cec9f86932fe2de9f3886059621903b262
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578171"
---
# <a name="master-planning-for-site-and-warehouse-coverage-warehouse-not-mandatory"></a><span data-ttu-id="5a393-104">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="5a393-104">Master planning for site and warehouse coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a393-105">In diesem Thema wird beschrieben wie ein Artikel, der Standort und Lagerort als Deckungsdimension hat, geplant wird.</span><span class="sxs-lookup"><span data-stu-id="5a393-105">This topic describes how an item that has site and warehouse as coverage dimensions is planned.</span></span> <span data-ttu-id="5a393-106">Die Lagerortdimension ist nicht obligatorisch.</span><span class="sxs-lookup"><span data-stu-id="5a393-106">The warehouse dimension is not mandatory.</span></span>

<span data-ttu-id="5a393-107">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="5a393-107">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="5a393-108">Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5a393-108">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span> <span data-ttu-id="5a393-109">Diese Einstellung kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5a393-109">This setting can't be modified.</span></span>
-   <span data-ttu-id="5a393-110">Die Lagerortdimension ist nicht auf obligatorisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a393-110">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="5a393-111">Der Lagerort ist unter Umständen bekannt, wird jedoch nicht in der Produktprogrammplanberechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="5a393-111">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="5a393-112">Die Standort- und Lagerortdimension werden für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a393-112">The site and warehouse dimensions are set for coverage planning.</span></span> <span data-ttu-id="5a393-113">Für die Disposition können auch andere Dimensionen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="5a393-113">Other dimensions may be set for coverage planning also.</span></span> <span data-ttu-id="5a393-114">Für diese ergeben sich jedoch keinerlei Auswirkungen durch die Funktion für mehrere Standorte.</span><span class="sxs-lookup"><span data-stu-id="5a393-114">However, they are not affected by the multisite functionality.</span></span>

<span data-ttu-id="5a393-115">In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="5a393-115">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="5a393-116">Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:</span><span class="sxs-lookup"><span data-stu-id="5a393-116">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="5a393-117">Der Lagerort ist auf Manuell festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a393-117">The warehouse is set to Manual.</span></span> <span data-ttu-id="5a393-118">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="5a393-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5a393-119">Wählen Sie auf dem Inforegister **Produktprogrammplanung** das Feld **Manuell**.</span><span class="sxs-lookup"><span data-stu-id="5a393-119">On the **Master planning** FastTab, see the **Manual** field.</span></span>
-   <span data-ttu-id="5a393-120">Für den Artikel ist die Artikeldeckung definiert.</span><span class="sxs-lookup"><span data-stu-id="5a393-120">Item coverage is defined for the item.</span></span> <span data-ttu-id="5a393-121">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="5a393-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5a393-122">Wählen Sie einen Artikel aus, und klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Plan** auf **Artikeldeckung**.</span><span class="sxs-lookup"><span data-stu-id="5a393-122">Select the item, and then, on the Action pane, on the **Plan** tab, click **Item coverage**.</span></span>
-   <span data-ttu-id="5a393-123">Für den Lagerort sind Auffüllbeziehungen definiert.</span><span class="sxs-lookup"><span data-stu-id="5a393-123">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="5a393-124">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="5a393-124">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="5a393-125">Wählen Sie auf dem Inforegister **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.</span><span class="sxs-lookup"><span data-stu-id="5a393-125">On the **Master planning** FastTab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="5a393-126">Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt.</span><span class="sxs-lookup"><span data-stu-id="5a393-126">The default order type is set to Production, Purchase order, or Kanban.</span></span> <span data-ttu-id="5a393-127">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="5a393-127">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="5a393-128">Wählen Sie einen Artikel aus, und klicken Sie anschließend im Aktivitätsbereich auf der Registerkarte **Plan** auf **Standardauftragseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="5a393-128">Select the item, and then, on the Action pane, on the **Plan** tab, click **Default order settings**.</span></span> <span data-ttu-id="5a393-129">Im Formular **Standardauftragseinstellungen** sehen Sie den **Standardauftragstyp**.</span><span class="sxs-lookup"><span data-stu-id="5a393-129">In the **Default order settings** form, see the **Default order type**.</span></span>

![Bedarf an Standort und Lagerort, Lagerort nicht obligatorisch](./media/multisitedemandexplosionscenarioforsiteandwarehousecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="5a393-131">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5a393-131">Additional resources</span></span>
--------

[<span data-ttu-id="5a393-132">Produktprogrammplanung und Funktion für mehrere Standorte</span><span class="sxs-lookup"><span data-stu-id="5a393-132">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="5a393-133">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="5a393-133">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5a393-134">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="5a393-134">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="5a393-135">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="5a393-135">Master planning - site coverage, warehouse not mandatory</span></span>](master-plan-site-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="5a393-136">Produktprogrammplanungslauf - Ermittlung der Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="5a393-136">Master planning - How the BOM version is determined</span></span>](master-plan-bom-version-determined.md)



