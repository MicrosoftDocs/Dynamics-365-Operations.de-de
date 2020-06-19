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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410951"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="8b741-104">Kostenberechnungsstufe</span><span class="sxs-lookup"><span data-stu-id="8b741-104">Cost calculation level</span></span>

<span data-ttu-id="8b741-105">Die Stücklistenebene (BOM) die **Kostenberechnungsstufe** benannt ist, schließt Fertigungsaufträge und Chargenaufträge von den Berechnungen aus.</span><span class="sxs-lookup"><span data-stu-id="8b741-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="8b741-106">Das System verwendet diese Ebene, wenn es Kostenberechnungen in Kalkulationsversionen ausführt.</span><span class="sxs-lookup"><span data-stu-id="8b741-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="8b741-107">In Prozessen wie Neuberechnung und Bestandsabschluss verwendet das System die **Kostenstufe** Stücklistenebene.</span><span class="sxs-lookup"><span data-stu-id="8b741-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="8b741-108">Das folgende einfache Szenario zeigt die Unterschiede zwischen der Stücklistenebene **Kostenberechnungsstufe** und **Kostenstufe**.</span><span class="sxs-lookup"><span data-stu-id="8b741-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="8b741-109">Sie haben drei Produkte: A, B und C. Produkt C ist die Komponente von Produkt B und Produkt B ist die Komponente von Produkt A.</span><span class="sxs-lookup"><span data-stu-id="8b741-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="8b741-110">**Kostenstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="8b741-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="8b741-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="8b741-111">**Product A:** 0</span></span>
    - <span data-ttu-id="8b741-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="8b741-112">**Product B:** 1</span></span>
    - <span data-ttu-id="8b741-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="8b741-113">**Product C:** 2</span></span>

- <span data-ttu-id="8b741-114">**Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="8b741-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="8b741-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="8b741-115">**Product A:** 0</span></span>
    - <span data-ttu-id="8b741-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="8b741-116">**Product B:** 1</span></span>
    - <span data-ttu-id="8b741-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="8b741-117">**Product C:** 2</span></span>

<span data-ttu-id="8b741-118">Anschließend wird ein Fertigungsauftrag für Produkt C erstellt und Produkt A zur Fertigungsauftragsstückliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8b741-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="8b741-119">Nachdem die Bestellung geschätzt wurde, werden die Stücklistenebenen folgendermaßen aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="8b741-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="8b741-120">**Kostenstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="8b741-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="8b741-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="8b741-121">**Product B:** 1</span></span>
    - <span data-ttu-id="8b741-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="8b741-122">**Product C:** 2</span></span>
    - <span data-ttu-id="8b741-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="8b741-123">**Product A:** 3</span></span>

- <span data-ttu-id="8b741-124">**Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="8b741-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="8b741-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="8b741-125">**Product A:** 0</span></span>
    - <span data-ttu-id="8b741-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="8b741-126">**Product B:** 1</span></span>
    - <span data-ttu-id="8b741-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="8b741-127">**Product C:** 2</span></span>

<span data-ttu-id="8b741-128">Dieses Verhalten stellt sicher, dass Änderungen an Fertigungsauftragsstücklisten keine Auswirkungen auf nachfolgende Kostenberechnungen haben.</span><span class="sxs-lookup"><span data-stu-id="8b741-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
