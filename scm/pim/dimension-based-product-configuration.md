---
title: Dimensionsbasierte Produktkonfiguration
description: "Die dimensionenbasierte Produktkonfiguration stellt eine einfache Lösung für das Erstellen vieler Produktvarianten aus einem einzigen Produktmaster und seiner Stückliste dar."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMConfigRule, BOMTable, ConfigChooseFromRoute, ConfigGroup, ConfigHierarchy, EcoResDimensionBasedConfiguration
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19821
ms.assetid: 4db9890b-306b-4be7-ba98-3be2094d561f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 89f01401f1d937a72ae7e59b784cf034b48aaf1f
ms.contentlocale: de-de
ms.lasthandoff: 07/18/2017

---

# <a name="dimension-based-product-configuration"></a><span data-ttu-id="08c9d-103">Dimensionsbasierte Produktkonfiguration</span><span class="sxs-lookup"><span data-stu-id="08c9d-103">Dimension-based product configuration</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="08c9d-104">Die dimensionenbasierte Produktkonfiguration stellt eine einfache Lösung für das Erstellen vieler Produktvarianten aus einem einzigen Produktmaster und seiner Stückliste dar.</span><span class="sxs-lookup"><span data-stu-id="08c9d-104">Dimension-based product configuration represents a simple solution for creating many product variants from a single product master and its bill of materials.</span></span>

<span data-ttu-id="08c9d-105">Die dimensionbasierte Produktkonfiguration ist eine von drei integrierten Produktkonfigurationstechnologien.</span><span class="sxs-lookup"><span data-stu-id="08c9d-105">Dimension-based product configuration is one of the three built-in product configuration technologies.</span></span> <span data-ttu-id="08c9d-106">Die beiden anderen Technologien sind vordefinierte Varianten und die einschränkungsbasierte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="08c9d-106">The two other technologies are predefined variants and constraint-based configuration.</span></span> <span data-ttu-id="08c9d-107">Alle drei Technologien verwenden einen Produktmaster als Ausgangspunkt und ermöglichen dem Benutzer, viele Produktvarianten für einen Produktmaster zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="08c9d-107">All three technologies use a product master as the starting point and allow the user to create many product variants for one product master.</span></span>

## <a name="key-concepts"></a><span data-ttu-id="08c9d-108">Schlüsselkonzepte</span><span class="sxs-lookup"><span data-stu-id="08c9d-108">Key concepts</span></span>
<span data-ttu-id="08c9d-109">Die dimensionbasierte Produktkonfiguration basiert auf den folgenden Schlüsselkonzepten:</span><span class="sxs-lookup"><span data-stu-id="08c9d-109">Dimension-based product configuration is based on the following key concepts:</span></span>

-   <span data-ttu-id="08c9d-110">Produktmaster</span><span class="sxs-lookup"><span data-stu-id="08c9d-110">Product masters</span></span>
-   <span data-ttu-id="08c9d-111">Konfigurationsproduktdimension</span><span class="sxs-lookup"><span data-stu-id="08c9d-111">Configuration product dimension</span></span>
-   <span data-ttu-id="08c9d-112">Variantengruppen</span><span class="sxs-lookup"><span data-stu-id="08c9d-112">Configuration groups</span></span>
-   <span data-ttu-id="08c9d-113">Stücklisten</span><span class="sxs-lookup"><span data-stu-id="08c9d-113">Bill of materials (BOM)</span></span>
-   <span data-ttu-id="08c9d-114">Variantenarbeitsplan</span><span class="sxs-lookup"><span data-stu-id="08c9d-114">Configuration route</span></span>
-   <span data-ttu-id="08c9d-115">Variantenregeln</span><span class="sxs-lookup"><span data-stu-id="08c9d-115">Configuration rules</span></span>

### <a name="product-masters"></a><span data-ttu-id="08c9d-116">Produktmaster</span><span class="sxs-lookup"><span data-stu-id="08c9d-116">Product masters</span></span>

<span data-ttu-id="08c9d-117">Ein Produktmaster ist der Ausgangspunkt für jeden Produktkonfigurationsprozess.</span><span class="sxs-lookup"><span data-stu-id="08c9d-117">A product master is the starting point for any product configuration process.</span></span> <span data-ttu-id="08c9d-118">Für die dimensionsbasierte Produktkonfiguration benötigen Sie einen Produktmaster mit eben dieser Konfigurationstechnologie und eine Produktdimensionsgruppe, die die Produktdimension der Konfiguration umfasst.</span><span class="sxs-lookup"><span data-stu-id="08c9d-118">For the dimension-based product configuration, you need a product master with this particular configuration technology and a product dimension group that includes the configuration product dimension.</span></span>

### <a name="configuration-product-dimension"></a><span data-ttu-id="08c9d-119">Konfigurationsproduktdimension</span><span class="sxs-lookup"><span data-stu-id="08c9d-119">Configuration product dimension</span></span>

<span data-ttu-id="08c9d-120">Die Produktdimension der Konfiguration wird dazu verwendet, die Produktvarianten für einen Produktmaster mithilfe der dimensionsbasierten Konfigurationstechnologie zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="08c9d-120">The configuration product dimension is used to identify the product variants for a product master with the dimension-based configuration technology.</span></span> <span data-ttu-id="08c9d-121">Der Konfigurationsdimensionswert wird vom Benutzer eingegeben und sollte helfen, die einzelnen Produktvarianten zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="08c9d-121">The configuration dimension value is entered by the user and should help to identify the individual product variants.</span></span>

### <a name="configuration-groups"></a><span data-ttu-id="08c9d-122">Variantengruppen</span><span class="sxs-lookup"><span data-stu-id="08c9d-122">Configuration groups</span></span>

<span data-ttu-id="08c9d-123">Variantengruppen werden in einem zentralen Repository definiert und können für alle dimensionsbasierten Produktkonfigurationsmodelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="08c9d-123">Configuration groups are defined in a central repository and can be used for all dimension-based product configuration models.</span></span> <span data-ttu-id="08c9d-124">Variantengruppen werden den einzelnen Stücklistenpositionen zugeordnet und halten eine Gruppe von Positionen zusammen, die sich gegenseitig ausschließen.</span><span class="sxs-lookup"><span data-stu-id="08c9d-124">Configuration groups are associated to the individual BOM lines and hold together a group of lines that are mutually exclusive.</span></span> <span data-ttu-id="08c9d-125">Das bedeutet, dass lediglich eine Position in einer Gruppe für eine einzelne Produktvariante ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="08c9d-125">This means that only one line in a group can be selected for a single product variant.</span></span>

### <a name="bill-of-materials-bom"></a><span data-ttu-id="08c9d-126">Stücklisten</span><span class="sxs-lookup"><span data-stu-id="08c9d-126">Bill of materials (BOM)</span></span>

<span data-ttu-id="08c9d-127">Die Stückliste stellt die Bausteine für eine dimensionsbasierte Produktkonfiguration dar.</span><span class="sxs-lookup"><span data-stu-id="08c9d-127">The BOM represent the building blocks for a dimension-based product configuration.</span></span> <span data-ttu-id="08c9d-128">Sie muss alle verschiedenen Produkte enthalten, die in einer beliebigen Produktvariante verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="08c9d-128">It must include all the different products that can be used in any product variant.</span></span> <span data-ttu-id="08c9d-129">Jede Position in der Stückliste kann auf eine Variantengruppe verweisen.</span><span class="sxs-lookup"><span data-stu-id="08c9d-129">Each line in the BOM can reference a configuration group.</span></span> <span data-ttu-id="08c9d-130">Wenn eine Position nicht auf eine Variantengruppe verweist, wird sie in alle Produktvarianten einbezogen.</span><span class="sxs-lookup"><span data-stu-id="08c9d-130">If a line doesn’t reference a configuration group, it will be included in all product variants.</span></span>

### <a name="configuration-route"></a><span data-ttu-id="08c9d-131">Variantenarbeitsplan</span><span class="sxs-lookup"><span data-stu-id="08c9d-131">Configuration route</span></span>

<span data-ttu-id="08c9d-132">Der Variantenarbeitsplan bestimmt die Reihenfolge der Variantengruppen, also wie diese dem Benutzer während des Produktkonfigurationsprozesses angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="08c9d-132">The configuration route determines the sequence of the configuration groups, as they will be displayed to the user during the product configuration process.</span></span>

### <a name="configuration-rules"></a><span data-ttu-id="08c9d-133">Variantenregeln</span><span class="sxs-lookup"><span data-stu-id="08c9d-133">Configuration rules</span></span>

<span data-ttu-id="08c9d-134">Die Variantenregeln helfen sicherzustellen, dass ein Produkt, das in einer Variantengruppe in einer Stückliste enthalten ist, entweder eine Einbeziehung oder einen Ausschluss eines Produkts in einer anderen Variantengruppe in der gleichen Stückliste erzwingt.</span><span class="sxs-lookup"><span data-stu-id="08c9d-134">The configuration rules represent a mechanism for ensuring that a product included in one configuration group in a BOM enforces either an inclusion or an exclusion of a product in a different configuration group in the same BOM.</span></span>

## <a name="product-modeling-process"></a><span data-ttu-id="08c9d-135">Produktmodellprozess</span><span class="sxs-lookup"><span data-stu-id="08c9d-135">Product modeling process</span></span>
<span data-ttu-id="08c9d-136">Die natürliche Reihenfolge bei der Erstellung eines Produktmodells für ein dimensionsbasiertes Produkt beginnt mit dem Definieren der relevanten Variantengruppen.</span><span class="sxs-lookup"><span data-stu-id="08c9d-136">The natural sequence for building a product model for a dimension-based product starts with defining the relevant configuration groups.</span></span> <span data-ttu-id="08c9d-137">Es muss sichergestellt werden, dass alle Produkte, die in der Stückliste verwendet werden, für das Unternehmen freigegeben wurden, für das dieses Produktmodell erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="08c9d-137">It is important to ensure that all products which will be used in the BOM have been relased to the company that the product model is built for.</span></span> <span data-ttu-id="08c9d-138">Mithilfe dieser Bausteine an vorhandenen Reservierungen für kann er die Stückliste erstellen und Variantengruppen zu den entsprechenden Stücklistenpositionen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="08c9d-138">With these building blocks in place, the user can create the BOM and assign configuration groups to all relevant BOM lines.</span></span> <span data-ttu-id="08c9d-139">Wird in der Stückliste abgeschlossen ist, kann ein Variantenarbeitsplan für die Einrichtungen der Variantengruppen in der korrekten Reihenfolge definiert werden.</span><span class="sxs-lookup"><span data-stu-id="08c9d-139">When the BOM is complete, a configuration route can be defined for ordering the configuration groups in the proper sequence.</span></span> <span data-ttu-id="08c9d-140">\[caption id="attachment\_282671" align="alignnone" width"1187"\][![ Der dimensionsbasierte Produktmodellprozess ](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png)Der dimensionsbasierte Produktmodellprozess \[/caption\] Wenn es bestimmte Produkte aus unterschiedlichen Konfigurationsgruppen gibt, die entweder zusammen verwendet werden müssen oder nicht zusammen verwendet werden dürfen, können Sie Variantenregeln erstellen, die diese Produktbeziehungen durchsetzen.</span><span class="sxs-lookup"><span data-stu-id="08c9d-140">\[caption id="attachment\_282671" align="alignnone" width="1187"\][![Dimension-based product modeling process](./media/dimension-based-product-modeling-process-v1.png)](./media/dimension-based-product-modeling-process-v1.png) Dimension-based product modeling process\[/caption\] If there are certain products from different configuration groups that either must or must not be used together, you can create configuration rules that will enforce these product relationships.</span></span> <span data-ttu-id="08c9d-141">Nachdem die Stückliste durch eine Stücklistenversion an einen dimensionsbasierten Produktmaster gebunden wurde und beide genehmigt und aktiviert wurden, können Sie Produktkonfigurationen erstellen und Namen für die einzelnen Konfigurationen eingeben.</span><span class="sxs-lookup"><span data-stu-id="08c9d-141">After the BOM has been tied together with a dimension-based product master through a BOM version and both have been approved and activated, you can create product configurations and enter a name for each configuration.</span></span> <span data-ttu-id="08c9d-142">Die Konfigurationen können definiert werden, bevor eine Buchung generiert wird, oder sie werden definiert, wenn eine bestimmte Konfiguration erforderlich wird.</span><span class="sxs-lookup"><span data-stu-id="08c9d-142">The configurations can be defined before any transactions are generated or it can be done when the need for a certain configuration occurs.</span></span>

### <a name="suggested-use"></a><span data-ttu-id="08c9d-143">Verwendungsempfehlung</span><span class="sxs-lookup"><span data-stu-id="08c9d-143">Suggested use</span></span>

<span data-ttu-id="08c9d-144">Die Technologie der dimensionsbasierten Konfiguration eignet sich insbesondere für Produkte mit begrenzter Variabilität, wenn die Kombination der Standardproduktdimensionen Größe, Farbe, Format und Konfiguration nicht für die Identifikation einer bestimmten Produktvariante geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="08c9d-144">The dimension-based configuration technology is best used for products with limited variability and the combination of the standard product dimensions size, color, style, and configuration is unsuitable for identifying a specific product variant.</span></span> <span data-ttu-id="08c9d-145">Ein Beispiel wäre ein Fahrrad mit Gestellgröße, Radgröße, Bremssystemen und unterschiedlichen Gängen.</span><span class="sxs-lookup"><span data-stu-id="08c9d-145">An example could be bicycle with frame height, wheel size, brake types, and different gears.</span></span>




