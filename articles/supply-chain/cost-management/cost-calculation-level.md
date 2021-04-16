---
title: Kostenberechnungsstufe
description: In diesem Thema wird die Stücklistenebene beschrieben, die als Kostenberechnungsstufe bezeichnet wird. Diese Stücklistenstufe schließt Produktions- und Chargenaufträge von ihren Berechnungen aus.
author: AndersGirke
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: f7cde239107528a6bc2aeb0e424d024d4f3fb2a6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839486"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="dbf26-104">Kostenberechnungsstufe</span><span class="sxs-lookup"><span data-stu-id="dbf26-104">Cost calculation level</span></span>

<span data-ttu-id="dbf26-105">Die Stücklistenebene (BOM) die **Kostenberechnungsstufe** benannt ist, schließt Fertigungsaufträge und Chargenaufträge von den Berechnungen aus.</span><span class="sxs-lookup"><span data-stu-id="dbf26-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="dbf26-106">Das System verwendet diese Ebene, wenn es Kostenberechnungen in Kalkulationsversionen ausführt.</span><span class="sxs-lookup"><span data-stu-id="dbf26-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="dbf26-107">In Prozessen wie Neuberechnung und Bestandsabschluss verwendet das System die **Kostenstufe** Stücklistenebene.</span><span class="sxs-lookup"><span data-stu-id="dbf26-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="dbf26-108">Das folgende einfache Szenario zeigt die Unterschiede zwischen der Stücklistenebene **Kostenberechnungsstufe** und **Kostenstufe**.</span><span class="sxs-lookup"><span data-stu-id="dbf26-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="dbf26-109">Sie haben drei Produkte: A, B und C. Produkt C ist die Komponente von Produkt B und Produkt B ist die Komponente von Produkt A.</span><span class="sxs-lookup"><span data-stu-id="dbf26-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="dbf26-110">**Kostenstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="dbf26-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="dbf26-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="dbf26-111">**Product A:** 0</span></span>
    - <span data-ttu-id="dbf26-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="dbf26-112">**Product B:** 1</span></span>
    - <span data-ttu-id="dbf26-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="dbf26-113">**Product C:** 2</span></span>

- <span data-ttu-id="dbf26-114">**Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="dbf26-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="dbf26-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="dbf26-115">**Product A:** 0</span></span>
    - <span data-ttu-id="dbf26-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="dbf26-116">**Product B:** 1</span></span>
    - <span data-ttu-id="dbf26-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="dbf26-117">**Product C:** 2</span></span>

<span data-ttu-id="dbf26-118">Anschließend wird ein Fertigungsauftrag für Produkt C erstellt und Produkt A zur Fertigungsauftragsstückliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dbf26-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="dbf26-119">Nachdem die Bestellung geschätzt wurde, werden die Stücklistenebenen folgendermaßen aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="dbf26-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="dbf26-120">**Kostenstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="dbf26-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="dbf26-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="dbf26-121">**Product B:** 1</span></span>
    - <span data-ttu-id="dbf26-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="dbf26-122">**Product C:** 2</span></span>
    - <span data-ttu-id="dbf26-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="dbf26-123">**Product A:** 3</span></span>

- <span data-ttu-id="dbf26-124">**Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="dbf26-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="dbf26-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="dbf26-125">**Product A:** 0</span></span>
    - <span data-ttu-id="dbf26-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="dbf26-126">**Product B:** 1</span></span>
    - <span data-ttu-id="dbf26-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="dbf26-127">**Product C:** 2</span></span>

<span data-ttu-id="dbf26-128">Dieses Verhalten stellt sicher, dass Änderungen an Fertigungsauftragsstücklisten keine Auswirkungen auf nachfolgende Kostenberechnungen haben.</span><span class="sxs-lookup"><span data-stu-id="dbf26-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]