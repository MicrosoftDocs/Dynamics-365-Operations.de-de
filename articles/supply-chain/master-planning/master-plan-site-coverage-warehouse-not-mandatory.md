---
title: Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch
description: "In diesem Thema wird beschrieben wie ein Artikel, der die Site-Dimension für den Deckung gesetzt hat, geplant wird."
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
ms.custom: 2474
ms.assetid: 316da918-67ae-43c5-baea-00ae559e29b0
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0b97f5f9a9a1447027e55d6c6b30253506caff70
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="master-planning-for-site-coverage-warehouse-not-mandatory"></a><span data-ttu-id="b105f-103">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="b105f-103">Master planning for site coverage, warehouse not mandatory</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b105f-104">In diesem Thema wird beschrieben wie ein Artikel, der die Site-Dimension für den Deckung gesetzt hat, geplant wird.</span><span class="sxs-lookup"><span data-stu-id="b105f-104">This topic describes how an item that has the site dimension set for coverage is planned.</span></span>

<span data-ttu-id="b105f-105">Für dieses Produktprogrammplanungsszenario müssen die folgenden Bedingungen erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="b105f-105">This master planning scenario involves the following conditions:</span></span>

-   <span data-ttu-id="b105f-106">Die Standortdimension ist als obligatorische Dimension festgelegt und muss für die Bedarfsbuchung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b105f-106">The site dimension is set to mandatory and must be entered on the demand transaction.</span></span>
-   <span data-ttu-id="b105f-107">Die Lagerortdimension ist nicht auf obligatorisch festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b105f-107">The warehouse dimension is not set to mandatory.</span></span> <span data-ttu-id="b105f-108">Der Lagerort ist unter Umständen bekannt, wird jedoch nicht in der Produktprogrammplanberechnung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b105f-108">The warehouse may be known, but it is not used in the master planning calculation.</span></span>
-   <span data-ttu-id="b105f-109">Die Standortdimension ist für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b105f-109">The site dimension is set for coverage planning.</span></span>
-   <span data-ttu-id="b105f-110">Die Lagerortdimension ist nicht für die Disposition festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b105f-110">The warehouse dimension is not set for coverage planning.</span></span> <span data-ttu-id="b105f-111">Deshalb werden Angebot und Nachfrage nach Standort und möglicherweise auch nach weiteren Dispositionsdimensionen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="b105f-111">Therefore, supply and demand are aggregated by site and, perhaps, other coverage-planned dimensions also.</span></span>

<span data-ttu-id="b105f-112">In der folgenden Grafik wird der Ablauf der Produktprogrammplanung veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="b105f-112">The following graphic illustrates how master planning proceeds.</span></span> <span data-ttu-id="b105f-113">Die Parameter, auf die in der Grafik Bezug genommen wird, sowie deren Position werden im Folgenden erläutert:</span><span class="sxs-lookup"><span data-stu-id="b105f-113">The parameters that are referred to in the graphic, and their locations, are as follows:</span></span>
-   <span data-ttu-id="b105f-114">Für den Artikel ist die Artikeldeckung definiert.</span><span class="sxs-lookup"><span data-stu-id="b105f-114">Item coverage is defined for the item.</span></span> <span data-ttu-id="b105f-115">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="b105f-115">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b105f-116">Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Artikeldeckung**.</span><span class="sxs-lookup"><span data-stu-id="b105f-116">Select the item, and then click **Plan &gt; Item coverage**.</span></span>
-   <span data-ttu-id="b105f-117">Für den Lagerort sind Auffüllbeziehungen definiert.</span><span class="sxs-lookup"><span data-stu-id="b105f-117">Refill relations are defined for the warehouse.</span></span> <span data-ttu-id="b105f-118">Klicken Sie auf **Lagerverwaltung &gt; Einstellungen &gt; Lageraufschlüsselung &gt; Lagerorte**.</span><span class="sxs-lookup"><span data-stu-id="b105f-118">Click **Inventory management &gt; Setup &gt; Inventory breakdown &gt; Warehouses**.</span></span> <span data-ttu-id="b105f-119">Wählen Sie auf der Registerkarte **Produktprogrammplanung** die Feldgruppe **Hauptlagerort**.</span><span class="sxs-lookup"><span data-stu-id="b105f-119">On the **Master planning** tab, see the **Main warehouse** field group.</span></span>
-   <span data-ttu-id="b105f-120">Der standardmäßige Auftragstyp wird zur Produktion, der Bestellung oder dem Kanban festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b105f-120">The default order type is set to Production, Purchase order or Kanban.</span></span> <span data-ttu-id="b105f-121">Klicken Sie auf **Produktinformationsverwaltung &gt; Produkte &gt; Freigegebene Produkte**.</span><span class="sxs-lookup"><span data-stu-id="b105f-121">Click **Product information management &gt; Products&gt; Released products**.</span></span> <span data-ttu-id="b105f-122">Wählen Sie den Artikel aus, und klicken Sie auf **Planen &gt; Standardauftragseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="b105f-122">Select the item, and then click **Plan &gt; Default order settings**.</span></span> <span data-ttu-id="b105f-123">Im Formular **Standardauftragseinstellungen** sehen Sie das Feld **Standardauftragstyp**.</span><span class="sxs-lookup"><span data-stu-id="b105f-123">In the **Default order settings** form, see the **Default order type** field.</span></span>

![Bedarf für Disposition an Standort, Lagerort nicht obligatorisch](./media/multisitedemandexplosionscenarioforsitecoveragewarehousenotmandatory.jpg)



<a name="additional-resources"></a><span data-ttu-id="b105f-125">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b105f-125">Additional resources</span></span>
--------

[<span data-ttu-id="b105f-126">Produktprogrammplanung und Funktion für mehrere Standorte</span><span class="sxs-lookup"><span data-stu-id="b105f-126">Master planning and multisite functionality</span></span>](master-plan-multisite-functionality.md)

[<span data-ttu-id="b105f-127">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="b105f-127">Master planning - site coverage, warehouse mandatory</span></span>](master-plan-site-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b105f-128">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort nicht obligatorisch</span><span class="sxs-lookup"><span data-stu-id="b105f-128">Master planning - site and warehouse coverage, warehouse not mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-not-mandatory.md)

[<span data-ttu-id="b105f-129">Produktprogrammplanungslauf - Standort- und Lagerdisposition, Lagerort obligatorisch</span><span class="sxs-lookup"><span data-stu-id="b105f-129">Master planning - site and warehouse coverage, warehouse mandatory</span></span>](master-plan-site-warehouse-coverage-warehouse-mandatory.md)

[<span data-ttu-id="b105f-130">Produktprogrammplanungslauf - Ermittlung der Stücklistenversion</span><span class="sxs-lookup"><span data-stu-id="b105f-130">Master planning - how the BOM version is determined</span></span>](master-plan-bom-version-determined.md)




