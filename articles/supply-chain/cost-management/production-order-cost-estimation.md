---
title: "Vorkalkulation für Produktionsauftrag"
description: "Dieser Artikel enthält Informationen zur Produktvorkalkulation. Die Produktvorkalkulation stellt die voraussichtlichen Material- und Kapazitätsverbrauchskosten für die Produktion eines Artikels in der geplanten Produktionsauftragsmenge bereit."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcTrans, InventCostTrans, ProdCalcTrans, ProdTableJour, ProdTableListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 80633
ms.assetid: b4625d10-c852-4fda-b718-79df458de0d4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 172bb55358c20ba80b1c32b05f1ae8e6aff8901f
ms.contentlocale: de-de
ms.lasthandoff: 07/18/2017

---

# <a name="production-order-cost-estimation"></a><span data-ttu-id="1705e-104">Vorkalkulation für Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="1705e-104">Production order cost estimation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1705e-105">Dieser Artikel enthält Informationen zur Produktvorkalkulation.</span><span class="sxs-lookup"><span data-stu-id="1705e-105">This article provides information about production cost estimation.</span></span> <span data-ttu-id="1705e-106">Die Produktvorkalkulation stellt die voraussichtlichen Material- und Kapazitätsverbrauchskosten für die Produktion eines Artikels in der geplanten Produktionsauftragsmenge bereit.</span><span class="sxs-lookup"><span data-stu-id="1705e-106">Production cost estimation provides the projected material and capacity consumption costs of producing an item in the planned production order quantity.</span></span> 

<span data-ttu-id="1705e-107">Nachdem Sie einen Produktionsauftrag erstellt haben, müssen Sie die Produktionskosten kalkulieren.</span><span class="sxs-lookup"><span data-stu-id="1705e-107">After you create a production order, you must estimate production costs.</span></span> <span data-ttu-id="1705e-108">Zweck ist es, den Artikel und den Arbeitsverbrauch für den Produktionsprozess zu schätzen, da diese Werte die Grundlage für die nachfolgenden Planungs- und Produktionsprozesse bilden.</span><span class="sxs-lookup"><span data-stu-id="1705e-108">The purpose is to estimate item and route consumption for the production process, because these estimates are used as the basis for subsequent scheduling and production processes.</span></span>

## <a name="production-cost-estimation"></a><span data-ttu-id="1705e-109">Produktionskosten vorkalkulieren</span><span class="sxs-lookup"><span data-stu-id="1705e-109">Production cost estimation</span></span>
<span data-ttu-id="1705e-110">Die Vorkalkulation für die Produktionskosten basiert auf den folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="1705e-110">Estimates of production costs are based on the following information:</span></span>

-   <span data-ttu-id="1705e-111">Die Menge auf dem Produktionsauftrag</span><span class="sxs-lookup"><span data-stu-id="1705e-111">The quantity on the production order</span></span>
-   <span data-ttu-id="1705e-112">Die Komponenten in den Produktionsstücklisten (BOMs)</span><span class="sxs-lookup"><span data-stu-id="1705e-112">The components on the production bills of materials (BOMs)</span></span>
-   <span data-ttu-id="1705e-113">Der Routingbetrieb im Produktionsplan</span><span class="sxs-lookup"><span data-stu-id="1705e-113">The routing operations in the production route</span></span>
-   <span data-ttu-id="1705e-114">Die indirekten Kosten, die auf die Komponenten sowie die Arbeitsgänge gelten</span><span class="sxs-lookup"><span data-stu-id="1705e-114">The indirect costs that apply to the components and operations</span></span>
-   <span data-ttu-id="1705e-115">Die Daten der aktiven Kosten ab dem Berechnungsdatum</span><span class="sxs-lookup"><span data-stu-id="1705e-115">The active cost data as of the calculation date</span></span>

<span data-ttu-id="1705e-116">Befindet sich ein Phantompositionsartikel in der Produktionsstückliste, werden in den Berechnungen die Komponenten sowie die Arbeitsgänge des Arbeitsplans für das Phantom berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="1705e-116">If there is a phantom line item on the production BOMs, the calculations reflect the phantom’s components and route operations.</span></span> <span data-ttu-id="1705e-117">Mithilfe der Vorkalkulationsaufgabe können Sie vorkalkulierte Kosten unter Verwendung aktualisierter Informationen neu berechnen.</span><span class="sxs-lookup"><span data-stu-id="1705e-117">You can use the estimation task to recalculate estimated costs so that they reflect updated information.</span></span> <span data-ttu-id="1705e-118">Bei diesen aktualisierten Informationen kann es sich beispielsweise um eine Änderung der Produktionsauftragsmenge, der Komponenten in den Produktionsstücklisten, der Arbeitsgänge des Produktionsarbeitsplans, der indirekten Kosten für diese Komponenten/Arbeitsgänge oder der Daten für aktive Kosten zum Datum der Neuberechnung handeln.</span><span class="sxs-lookup"><span data-stu-id="1705e-118">For example, the updated information might be changes to the quantity on the production order, the components on the production BOMs, the routing operations in the production route, the indirect costs that apply to these components and operations, or the active cost data as of the recalculation date.</span></span> <span data-ttu-id="1705e-119">Anhand der Berechnung der vorkalkulierten Kosten wird auf Basis eines Kosten-plus-Aufschlag-Ansatzes auch ein Verkaufspreisvorschlag für den Produktionsartikel erstellt.</span><span class="sxs-lookup"><span data-stu-id="1705e-119">The calculations of estimated cost also suggest a sales price for the production item, based on a cost-plus-markup approach.</span></span> <span data-ttu-id="1705e-120">Die Berechnung der vorkalkulierten Kosten kann optional auch für Referenzaufträge verwendet werden, bei denen es sich um mit dem Produktionsauftrag verknüpfte Produktionsaufträge handelt.</span><span class="sxs-lookup"><span data-stu-id="1705e-120">The calculations of estimated cost can optionally apply to reference orders that reflect other production orders that are linked to the production order.</span></span>

## <a name="view-the-estimated-costs"></a><span data-ttu-id="1705e-121">Die vorkalkulierten Kosten anzeigen</span><span class="sxs-lookup"><span data-stu-id="1705e-121">View the estimated costs</span></span>
<span data-ttu-id="1705e-122">Nach Ausführung der Vorkalkulation, können Sie die Ergebnisse auf der Seite **Preiskalkulation** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="1705e-122">After you run estimation, you can view the results on the **Price calculation** page.</span></span> <span data-ttu-id="1705e-123">Bei der Vorkalkulation werden die folgenden Werte berechnet:</span><span class="sxs-lookup"><span data-stu-id="1705e-123">The estimation calculates the following values:</span></span>

-   <span data-ttu-id="1705e-124">**Produktionskosten** – Dies ist die oberste Position der Vorkalkulation.</span><span class="sxs-lookup"><span data-stu-id="1705e-124">**Production cost** – The production cost is the top line of the estimate.</span></span> <span data-ttu-id="1705e-125">Es werden die Gesamtkosten der Ausführung des Produktionsauftrags und der Gesamtverkaufspreis für die Produktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="1705e-125">It shows the complete cost of running the production order and the total sales price for the production.</span></span> <span data-ttu-id="1705e-126">Dies ist die Summe aller Kostenpositionen in der Vorkalkulation.</span><span class="sxs-lookup"><span data-stu-id="1705e-126">It's the sum of all the cost lines on the estimate.</span></span>
-   <span data-ttu-id="1705e-127">**Arbeitsplan- oder Ressourcenkosten** - Arbeitsplan- oder Ressourcenkosten sind die Kosten für die Produktionsaufträge.</span><span class="sxs-lookup"><span data-stu-id="1705e-127">**Route or resource costs** – Route or resource costs are the costs for the production operations.</span></span> <span data-ttu-id="1705e-128">Die enthalten die Kosten von Elementen wie Rüstzeit, Bearbeitungszeit und Gemeinkosten.</span><span class="sxs-lookup"><span data-stu-id="1705e-128">They include the cost of elements such as setup time, run time, and overhead.</span></span>
-   <span data-ttu-id="1705e-129">**Materialkosten** – Dies sind die Kosten und Preise der BOM-Komponenten, die erforderlich sind, um den Artikel zu produzieren.</span><span class="sxs-lookup"><span data-stu-id="1705e-129">**Material costs** – Material costs are the costs and prices of the BOM components that are required in order to produce the item.</span></span> <span data-ttu-id="1705e-130">Diese Kosten wurden zuvor erstellt und in das System eingegeben.</span><span class="sxs-lookup"><span data-stu-id="1705e-130">These costs have previously been established and entered into the system.</span></span>

## <a name="other-uses-of-cost-estimation"></a><span data-ttu-id="1705e-131">Sonstige Verwendung einer Kostenvorkalkulation</span><span class="sxs-lookup"><span data-stu-id="1705e-131">Other uses of cost estimation</span></span>
<span data-ttu-id="1705e-132">Eine Vorkalkulation stellt auch die folgenden Informationen bereit:</span><span class="sxs-lookup"><span data-stu-id="1705e-132">A cost estimate also provides the following information:</span></span>

-   <span data-ttu-id="1705e-133">Aussagekräftige Preisangebote</span><span class="sxs-lookup"><span data-stu-id="1705e-133">Meaningful price quotations</span></span>
-   <span data-ttu-id="1705e-134">Vorkalkulation der Rentabilität des Auftrags</span><span class="sxs-lookup"><span data-stu-id="1705e-134">Estimates of the profitability of the order</span></span>
-   <span data-ttu-id="1705e-135">Vorkalkulation des Rohmaterialverbrauchs</span><span class="sxs-lookup"><span data-stu-id="1705e-135">Estimates of raw material usage</span></span>
-   <span data-ttu-id="1705e-136">Vergleiche von Kosteninformationen aus vorherigen Produktionen</span><span class="sxs-lookup"><span data-stu-id="1705e-136">Comparisons of cost information from previous productions</span></span>
-   <span data-ttu-id="1705e-137">Budget- und Planungsinformationen</span><span class="sxs-lookup"><span data-stu-id="1705e-137">Budget and forecasting information</span></span>
-   <span data-ttu-id="1705e-138">Vorkalkulation der zur Verwaltung bestimmter Kosten erforderlichen Produktionsgröße</span><span class="sxs-lookup"><span data-stu-id="1705e-138">Estimates of the production size that is required in order to maintain a particular cost</span></span>





