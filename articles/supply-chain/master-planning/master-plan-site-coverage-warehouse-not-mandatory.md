---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch
description: In diesem Thema wird beschrieben wie ein Artikel, der die Site-Dimension für den Deckung gesetzt hat, geplant wird.
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0f4cde5c570148ca58c4ea583a8f538a72d4957d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4428937"
---
# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="72e26-103">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="72e26-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72e26-104">In diesem Thema wird beschrieben wie ein Artikel, der die Site-Dimension für den Deckung gesetzt hat, geplant wird.</span><span class="sxs-lookup"><span data-stu-id="72e26-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="72e26-105">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="72e26-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="72e26-106">Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="72e26-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="72e26-107">Die Lagerortdimension ist nicht auf obligatorisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72e26-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="72e26-108">Der Lagerort ist unter Umständen bekannt, wird jedoch nicht in der Produktprogrammplanberechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="72e26-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="72e26-109">Die Standortdimension ist für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72e26-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="72e26-110">Die Lagerortdimension ist nicht für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72e26-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="72e26-111">Deshalb werden Angebot und Nachfrage nach Standort und möglicherweise auch nach weiteren Dispositionsdimensionen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="72e26-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="72e26-112">In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="72e26-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="72e26-113">Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:</span><span class="sxs-lookup"><span data-stu-id="72e26-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="72e26-114">Für den Artikel ist die Artikeldeckung definiert.</span><span class="sxs-lookup"><span data-stu-id="72e26-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="72e26-115">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="72e26-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="72e26-116">Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Artikeldeckung**.</span><span class="sxs-lookup"><span data-stu-id="72e26-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="72e26-117">Für den Lagerort sind Auffüllbeziehungen definiert.</span><span class="sxs-lookup"><span data-stu-id="72e26-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="72e26-118">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="72e26-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="72e26-119">Wählen Sie auf der Registerkarte **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.</span><span class="sxs-lookup"><span data-stu-id="72e26-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="72e26-120">Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt.</span><span class="sxs-lookup"><span data-stu-id="72e26-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="72e26-121">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="72e26-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="72e26-122">Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Standardauftragseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="72e26-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="72e26-123">Im Formular **Standardauftragseinstellungen** sehen Sie das Feld **Standardauftragstyp**.</span><span class="sxs-lookup"><span data-stu-id="72e26-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Bedarf für Disposition an Standort, Lagerort nicht obligatorisch](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="72e26-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="72e26-125">Additional resources</span></span>
--------

[<span data-ttu-id="72e26-126">Hauptpläne und Funktion für mehrere Standorte – Übersicht</span><span class="sxs-lookup"><span data-stu-id="72e26-126">Master planning and multisite functionality overview</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="72e26-127">Produktprogrammplanung für Disposition an Standort und Lagerort, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="72e26-127">Master planning for site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="72e26-128">Hauptplanung für Standortdeckung, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="72e26-128">Master planning for site coverage, mandatory warehouse</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="72e26-129">Hauptplanung für Standortdeckung, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="72e26-129">Master planning for site coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="72e26-130">Die Stücklistenversion bestimmen</span><span class="sxs-lookup"><span data-stu-id="72e26-130">Determine the BOM version</span></span>](master-plan-bom-version-determined.md)



