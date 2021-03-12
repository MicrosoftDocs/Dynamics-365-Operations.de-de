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
ms.openlocfilehash: 42088d8c005cf3fc04e768f1b8e8c8ca0b8c6993
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967727"
---
# <a name="cost-calculation-level"></a><span data-ttu-id="64c28-104">Kostenberechnungsstufe</span><span class="sxs-lookup"><span data-stu-id="64c28-104">Cost calculation level</span></span>

<span data-ttu-id="64c28-105">Die Stücklistenebene (BOM) die **Kostenberechnungsstufe** benannt ist, schließt Fertigungsaufträge und Chargenaufträge von den Berechnungen aus.</span><span class="sxs-lookup"><span data-stu-id="64c28-105">The bill of materials (BOM) level that is named **Cost calculation level** excludes production orders and batch orders from its calculations.</span></span> <span data-ttu-id="64c28-106">Das System verwendet diese Ebene, wenn es Kostenberechnungen in Kalkulationsversionen ausführt.</span><span class="sxs-lookup"><span data-stu-id="64c28-106">The system uses this level when it runs cost calculations in costing versions.</span></span> <span data-ttu-id="64c28-107">In Prozessen wie Neuberechnung und Bestandsabschluss verwendet das System die **Kostenstufe** Stücklistenebene.</span><span class="sxs-lookup"><span data-stu-id="64c28-107">In processes such as recalculation and inventory close, the system uses the **Costing level** BOM level instead.</span></span>

<span data-ttu-id="64c28-108">Das folgende einfache Szenario zeigt die Unterschiede zwischen der Stücklistenebene **Kostenberechnungsstufe** und **Kostenstufe**.</span><span class="sxs-lookup"><span data-stu-id="64c28-108">The following simple scenario shows the differences between the **Cost calculation level** BOM level and the **Costing level** BOM level.</span></span>

<span data-ttu-id="64c28-109">Sie haben drei Produkte: A, B und C. Produkt C ist die Komponente von Produkt B und Produkt B ist die Komponente von Produkt A.</span><span class="sxs-lookup"><span data-stu-id="64c28-109">You have three products: A, B, and C. Product C is the component of product B, and product B is the component of product A.</span></span>

- <span data-ttu-id="64c28-110">**Kostenstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="64c28-110">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="64c28-111">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="64c28-111">**Product A:** 0</span></span>
    - <span data-ttu-id="64c28-112">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="64c28-112">**Product B:** 1</span></span>
    - <span data-ttu-id="64c28-113">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="64c28-113">**Product C:** 2</span></span>

- <span data-ttu-id="64c28-114">**Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="64c28-114">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="64c28-115">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="64c28-115">**Product A:** 0</span></span>
    - <span data-ttu-id="64c28-116">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="64c28-116">**Product B:** 1</span></span>
    - <span data-ttu-id="64c28-117">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="64c28-117">**Product C:** 2</span></span>

<span data-ttu-id="64c28-118">Anschließend wird ein Fertigungsauftrag für Produkt C erstellt und Produkt A zur Fertigungsauftragsstückliste hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="64c28-118">A production order for product C is then created, and product A is added to the production order BOM.</span></span> <span data-ttu-id="64c28-119">Nachdem die Bestellung geschätzt wurde, werden die Stücklistenebenen folgendermaßen aktualisiert:</span><span class="sxs-lookup"><span data-stu-id="64c28-119">After the order is estimated, BOM levels are updated in the following way:</span></span>

- <span data-ttu-id="64c28-120">**Kostenstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="64c28-120">**Costing level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="64c28-121">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="64c28-121">**Product B:** 1</span></span>
    - <span data-ttu-id="64c28-122">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="64c28-122">**Product C:** 2</span></span>
    - <span data-ttu-id="64c28-123">**Produkt A:** 3</span><span class="sxs-lookup"><span data-stu-id="64c28-123">**Product A:** 3</span></span>

- <span data-ttu-id="64c28-124">**Kostenberechnungsstufe** weist die folgenden Stücklistenebenen zu:</span><span class="sxs-lookup"><span data-stu-id="64c28-124">**Cost calculation level** assigns the following BOM levels:</span></span>

    - <span data-ttu-id="64c28-125">**Produkt A:** 0</span><span class="sxs-lookup"><span data-stu-id="64c28-125">**Product A:** 0</span></span>
    - <span data-ttu-id="64c28-126">**Produkt B:** 1</span><span class="sxs-lookup"><span data-stu-id="64c28-126">**Product B:** 1</span></span>
    - <span data-ttu-id="64c28-127">**Produkt C:** 2</span><span class="sxs-lookup"><span data-stu-id="64c28-127">**Product C:** 2</span></span>

<span data-ttu-id="64c28-128">Dieses Verhalten stellt sicher, dass Änderungen an Fertigungsauftragsstücklisten keine Auswirkungen auf nachfolgende Kostenberechnungen haben.</span><span class="sxs-lookup"><span data-stu-id="64c28-128">This behavior ensures that changes to production order BOMs don't affect subsequent cost calculations.</span></span>
