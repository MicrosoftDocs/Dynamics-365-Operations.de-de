---
title: Kostenberechnungsstufe
description: In diesem Thema wird die Stücklistenebene beschrieben, die als Kostenberechnungsstufe bezeichnet wird. Diese Stücklistenstufe schließt Produktions- und Chargenaufträge von ihren Berechnungen aus.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 1cfbbb6aadbd24a0352776285f6c60ff10f59549
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251025"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="59646-104">Kostenberechnungsstufe</span><span class="sxs-lookup"><span data-stu-id="59646-104">Cost calculation level</span></span>

<span data-ttu-id="59646-105">Die Stücklistenebene (BOM) die **Kostenberechnungsstufe** benannt ist, schließt Fertigungsaufträge und Chargenaufträge von den Berechnungen aus.</span><span class="sxs-lookup"><span data-stu-id="59646-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="59646-106">Das System verwendet diese Ebene, wenn es Kostenberechnungen in Kalkulationsversionen ausführt.</span><span class="sxs-lookup"><span data-stu-id="59646-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="59646-107">In Prozessen wie Neuberechnung und Bestandsabschluss verwendet das System die **Kostenstufe** Stücklistenebene.</span><span class="sxs-lookup"><span data-stu-id="59646-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="59646-108">Das folgende einfache Szenario zeigt die Unterschiede zwischen der Stücklistenebene **Kostenberechnungsstufe** und **Kostenstufe**.</span><span class="sxs-lookup"><span data-stu-id="59646-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="59646-109">Sie haben drei Produkte: A, B und C. Produkt C ist die Komponente von Produkt B und Produkt B ist die Komponente von Produkt A.</span><span class="sxs-lookup"><span data-stu-id="59646-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="59646-110">**Kostenstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="59646-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="59646-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="59646-111">**Product A:** 0</span></span>
    - <span data-ttu-id="59646-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="59646-112">**Product B:** 1</span></span>
    - <span data-ttu-id="59646-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="59646-113">**Product C:** 2</span></span>

- <span data-ttu-id="59646-114">**Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="59646-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="59646-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="59646-115">**Product A:** 0</span></span>
    - <span data-ttu-id="59646-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="59646-116">**Product B:** 1</span></span>
    - <span data-ttu-id="59646-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="59646-117">**Product C:** 2</span></span>

<span data-ttu-id="59646-118">Anschließend wird ein Fertigungsauftrag für Produkt C erstellt und Produkt A zur Fertigungsauftragsstückliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="59646-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="59646-119">Nachdem die Bestellung geschätzt wurde, werden die Stücklistenebenen folgendermaßen aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="59646-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="59646-120">**Kostenstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="59646-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="59646-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="59646-121">**Product B:** 1</span></span>
    - <span data-ttu-id="59646-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="59646-122">**Product C:** 2</span></span>
    - <span data-ttu-id="59646-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="59646-123">**Product A:** 3</span></span>

- <span data-ttu-id="59646-124">**Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="59646-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="59646-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="59646-125">**Product A:** 0</span></span>
    - <span data-ttu-id="59646-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="59646-126">**Product B:** 1</span></span>
    - <span data-ttu-id="59646-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="59646-127">**Product C:** 2</span></span>

<span data-ttu-id="59646-128">Dieses Verhalten stellt sicher, dass Änderungen an Fertigungsauftragsstücklisten keine Auswirkungen auf nachfolgende Kostenberechnungen haben.</span><span class="sxs-lookup"><span data-stu-id="59646-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]