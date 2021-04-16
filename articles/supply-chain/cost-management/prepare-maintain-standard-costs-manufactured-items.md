---
title: Vorbereiten der Verwaltung von Standardkosten für produzierte Artikel
description: In diesem Thema werden die Schritte zur Vorbereitung der Kostenverwaltung für produzierte Artikel beschrieben.
author: AndersGirke
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6944782ac236a3f414b1cadfb12b0f0d8c1115b9
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5821512"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a><span data-ttu-id="19a50-103">Vorbereiten der Verwaltung von Standardkosten für produzierte Artikel</span><span class="sxs-lookup"><span data-stu-id="19a50-103">Prepare to maintain standard costs for manufactured items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19a50-104">In diesem Thema werden die Schritte zur Vorbereitung der Kostenverwaltung für produzierte Artikel beschrieben.</span><span class="sxs-lookup"><span data-stu-id="19a50-104">This topic describes the steps for preparing to maintain costs for manufactured items.</span></span> <span data-ttu-id="19a50-105">Die Schritte für produzierte Artikel unterscheiden sich etwas von den Schritten für eingekaufte Artikel.</span><span class="sxs-lookup"><span data-stu-id="19a50-105">The steps for manufactured items differ slightly from the steps for purchased items.</span></span>

<span data-ttu-id="19a50-106">Richtlinien, die produzierten Artikeln zugewiesen sind, können sich auf die Kostenberechnungen für die übergeordneten produzierten Artikel auswirken.</span><span class="sxs-lookup"><span data-stu-id="19a50-106">Policies that are assigned to manufactured items can affect the cost calculations for the parent manufactured items.</span></span> <span data-ttu-id="19a50-107">Gehen Sie zur Vorbereitung der Kostenverwaltung für produzierte Artikel folgendermaßen vor.</span><span class="sxs-lookup"><span data-stu-id="19a50-107">To prepare to maintain costs for manufactured items, follow these steps.</span></span>

1. <span data-ttu-id="19a50-108">Weisen Sie dem produzierten Artikel eine Artikelmodellgruppe zu.</span><span class="sxs-lookup"><span data-stu-id="19a50-108">Assign an item model group to the manufactured item.</span></span> 

   <span data-ttu-id="19a50-109">Die Artikelmodellgruppe bestimmt, dass Standardkosten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19a50-109">The item model group identifies that standard costs will be used.</span></span>

2. <span data-ttu-id="19a50-110">Weisen Sie dem produzierten Artikel eine Artikelgruppe zu.</span><span class="sxs-lookup"><span data-stu-id="19a50-110">Assign an item group to the manufactured item.</span></span> 

   <span data-ttu-id="19a50-111">Die Artikelgruppe enthält Sachkonten für den produzierten Artikel.</span><span class="sxs-lookup"><span data-stu-id="19a50-111">The item group contains ledger accounts that apply to the manufactured item.</span></span> <span data-ttu-id="19a50-112">Die Sachkonten für einen produzierten Artikel mit einem Lagermodell vom Typ „Standardkosten” umfassen mehrere Produktionsabweichungen sowie die Abweichung bei Kostenänderung und die Neubewertung der Lagerkosten.</span><span class="sxs-lookup"><span data-stu-id="19a50-112">The ledger accounts for a manufactured item that has a standard cost inventory model include several production variances, the cost change variance, and the inventory cost revaluation.</span></span>

3. <span data-ttu-id="19a50-113">Weisen Sie dem Artikel die Lagermaßeinheit zu.</span><span class="sxs-lookup"><span data-stu-id="19a50-113">Assign the inventory unit of measure to the item.</span></span> 

   <span data-ttu-id="19a50-114">Die Kosten des Artikels werden stets in der Lagermaßeinheit des Artikels ausgedrückt.</span><span class="sxs-lookup"><span data-stu-id="19a50-114">The item's costs are always expressed in the item's inventory unit of measure.</span></span>

4. <span data-ttu-id="19a50-115">Weisen Sie dem produzierten Artikel nur dann eine Kostengruppe zu, wenn der Artikel als eingekaufter Artikel behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="19a50-115">Don't assign a cost group to the manufactured item unless the item will be treated as a purchased item.</span></span>

5. <span data-ttu-id="19a50-116">Weisen Sie dem produzierten Artikel eine Stücklisten-Berechnungsgruppe zu.</span><span class="sxs-lookup"><span data-stu-id="19a50-116">Assign a bill of materials (BOM) calculation group to the manufactured item.</span></span> 

   <span data-ttu-id="19a50-117">Durch die Stücklisten-Berechnungsgruppe des Artikels werden Warnbedingungen definiert, die gelten.</span><span class="sxs-lookup"><span data-stu-id="19a50-117">The item's BOM calculation group defines warning conditions that apply.</span></span> <span data-ttu-id="19a50-118">Dadurch können, wenn eine Stücklistenberechnung erfolgt, Warnmeldungen über mögliche Quellen von Berechnungsfehlern generiert werden.</span><span class="sxs-lookup"><span data-stu-id="19a50-118">In that way, when a BOM calculation is done, warning messages can be generated about possible sources of calculation errors.</span></span> <span data-ttu-id="19a50-119">So kann beispielsweise durch eine Warnmeldung darauf hingewiesen werden, dass keine aktive Stückliste oder kein aktiver Arbeitsplan vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="19a50-119">For example, a warning message can identify when an active BOM or route doesn't exist.</span></span> <span data-ttu-id="19a50-120">Die Stücklisten-Kalkulationsgruppe enthält eine Richtlinie vom Typ „Stücklistenauflösung beenden”, durch die angegeben wird, wann ein produzierter Artikel als eingekaufter Artikel behandelt werden soll.</span><span class="sxs-lookup"><span data-stu-id="19a50-120">The BOM calculation group contains a stop explosion policy that indicates when a manufactured item should be treated as a purchased item.</span></span>

6. <span data-ttu-id="19a50-121">Wenn der produzierte Artikel konstante Kosten aufweist, weisen Sie ihm eine Standardauftragsmenge zu.</span><span class="sxs-lookup"><span data-stu-id="19a50-121">If the manufactured item has constant costs, assign a standard order quantity to it.</span></span> 

   <span data-ttu-id="19a50-122">Die Standardauftragsmenge fungiert als Abrechnungspostengröße für die Amortisierung konstanter Kosten.</span><span class="sxs-lookup"><span data-stu-id="19a50-122">The standard order quantity is an accounting lot size for amortizing constant costs.</span></span> <span data-ttu-id="19a50-123">Beispiele der konstanten Kosten umfassen Rüstzeiten bei Routingarbeitsgängen und eine konstante Komponentenmenge in der Stückliste.</span><span class="sxs-lookup"><span data-stu-id="19a50-123">Examples of constant costs include setup times in routing operations and a constant component quantity in the BOM.</span></span>

7. <span data-ttu-id="19a50-124">Definieren Sie die Stückliste für den produzierten Artikel.</span><span class="sxs-lookup"><span data-stu-id="19a50-124">Define the BOM for the manufactured item.</span></span> 

   <span data-ttu-id="19a50-125">Für den produzierten Artikel können mehrere Stücklistenversionen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="19a50-125">One or more BOM versions can be defined for the manufactured item.</span></span> <span data-ttu-id="19a50-126">Vergewissern Sie sich, dass die gewünschten Versionen als „Genehmigt” und „Aktiv” markiert sind und das gewünschte Gültigkeitsdatum besitzen.</span><span class="sxs-lookup"><span data-stu-id="19a50-126">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="19a50-127">Die Stücklistenversion kann als unternehmensweite oder als standortspezifische Version verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="19a50-127">The BOM version can be company-wide or site-specific.</span></span>

8. <span data-ttu-id="19a50-128">Definieren Sie den Arbeitsplan für den produzierten Artikel.</span><span class="sxs-lookup"><span data-stu-id="19a50-128">Define the routing for the manufactured item.</span></span> 

   <span data-ttu-id="19a50-129">Für den produzierten Artikel können mehrere Arbeitsplanversionen definiert werden.</span><span class="sxs-lookup"><span data-stu-id="19a50-129">One or more route versions can be defined for the manufactured item.</span></span> <span data-ttu-id="19a50-130">Vergewissern Sie sich, dass die gewünschten Versionen als „Genehmigt” und „Aktiv” markiert sind und das gewünschte Gültigkeitsdatum besitzen.</span><span class="sxs-lookup"><span data-stu-id="19a50-130">Verify that the versions that you want have been marked as approved and active, and that they have the effective dates that you want.</span></span> <span data-ttu-id="19a50-131">Die Arbeitsplanversion muss standortspezifisch sein.</span><span class="sxs-lookup"><span data-stu-id="19a50-131">The route version must be site-specific.</span></span>

<span data-ttu-id="19a50-132">Wenn Sie Routinginformationen für die Nachkalkulation verwenden möchten, sind weitere Vorbereitungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="19a50-132">If you want to use routing information for costing purposes, additional preparation steps are required.</span></span> <span data-ttu-id="19a50-133">So muss beispielsweise sichergestellt werden, dass die dem Arbeitsgang des Arbeitsplans zugewiesenen Kostenkategorien korrekt und vollständig sind.</span><span class="sxs-lookup"><span data-stu-id="19a50-133">For example, the cost categories that are assigned to routing operations must be correct and completed.</span></span>

<a name="related-topics"></a><span data-ttu-id="19a50-134">Verwandte Themen</span><span class="sxs-lookup"><span data-stu-id="19a50-134">Related topics</span></span>
--------

[<span data-ttu-id="19a50-135">Amortisierung konstanter Kosten für einen produzierten Artikel</span><span class="sxs-lookup"><span data-stu-id="19a50-135">Amortize constant costs for a manufactured item</span></span>](amortize-constant-costs-manufactured-item.md)

[<span data-ttu-id="19a50-136">Einrichten von Produkten, die produziert werden oder beschafft werden</span><span class="sxs-lookup"><span data-stu-id="19a50-136">Set up products that can be produced or procured</span></span>](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]