---
title: "Amortisierung konstanter Kosten für einen produzierten Artikel"
description: "Die konstanten Kosten eines produzierten Artikels beinhalten die Arbeitsgangrüstzeiten sowie die Komponenten mit einer konstanten Menge oder einem konstanten Schrottwert."
author: YuyuScheller
manager: AnnBe
ms.date: 04/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.dyn365.ops.intro: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f8c72cf675d99f78c03ae2f2fef53b51fbf4bd8b
ms.contentlocale: de-de
ms.lasthandoff: 08/29/2017

---

# <a name="amortize-constant-costs-for-a-manufactured-item"></a><span data-ttu-id="1d17f-103">Amortisierung konstanter Kosten für einen produzierten Artikel</span><span class="sxs-lookup"><span data-stu-id="1d17f-103">Amortize constant costs for a manufactured item</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1d17f-104">Die konstanten Kosten eines produzierten Artikels beinhalten die Arbeitsgangrüstzeiten sowie die Komponenten mit einer konstanten Menge oder einem konstanten Schrottwert.</span><span class="sxs-lookup"><span data-stu-id="1d17f-104">A manufactured item’s constant costs reflect the operation setup times and the components that have a constant quantity or a constant scrap amount.</span></span> 

<span data-ttu-id="1d17f-105">Das Konzept der Nachkalkulationslosgröße dient zum Amortisieren dieser konstanten Kosten in den berechneten Kosten eines produzierten Artikels.</span><span class="sxs-lookup"><span data-stu-id="1d17f-105">The concept of a costing lot size is used to amortize these constant costs in the calculated cost of a manufactured item.</span></span> <span data-ttu-id="1d17f-106">Dieses Konzept besitzt mehrere Synonyme, von denen eines "Abrechnungslosgröße" lautet.</span><span class="sxs-lookup"><span data-stu-id="1d17f-106">This concept has several synonyms, one of which is accounting lot size.</span></span> <span data-ttu-id="1d17f-107">Selbiges gilt auch für das Konzept der Amortisierung konstanter Kosten, das beispielsweise auch als proportionale konstante Kosten bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="1d17f-107">The concept of amortizing constant costs also has several synonyms, one of which is proportional constant costs.</span></span>
<span data-ttu-id="1d17f-108">Die Menge einer Nachkalkulationslosgröße für einen produzierten Artikel fließt in die Herstellkostenkalkulation ein.</span><span class="sxs-lookup"><span data-stu-id="1d17f-108">The quantity of a costing lot size for a manufactured item is used in a bill of material (BOM) calculation.</span></span> <span data-ttu-id="1d17f-109">Die Menge ist von der Initiierung und Ausführung der Herstellkostenkalkulation abhängig. Dies wird im Folgenden veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="1d17f-109">The quantity depends on how you initiate and perform the BOM calculation, as illustrated by the following:</span></span>
-   <span data-ttu-id="1d17f-110">Standardberechnungsmenge in der Herstellkostenkalkulation eines Artikels − Die Standardauftragsmenge des Artikels (für das Lager) fungiert als Standardwert für dessen Nachkalkulationslosgröße, bei dem Standardwert handelt es sich jedoch möglicherweise um eine größere Menge, die ein Vielfaches der Auftragsmenge für den Artikel darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d17f-110">Default calculation quantity in an item’s BOM calculation − The item’s standard order quantity for inventory acts as the costing lot size, but the default value might be a greater quantity to reflect the item’s order quantity multiple.</span></span> <span data-ttu-id="1d17f-111">Die Standard-Auftragsmenge sowie das Vielfache werden in den Standardauftragseinstellungen oder in den standortspezifischen Auftragseinstellungen definiert.</span><span class="sxs-lookup"><span data-stu-id="1d17f-111">The item’s standard order quantity and multiple can be defined within its default order settings or site-specific order settings.</span></span>
-   <span data-ttu-id="1d17f-112">Angegebene Berechnungsmenge in der Herstellkostenkalkulation eines Artikels − Die angegebene Berechnungsmenge fungiert als Nachkalkulationslosgröße für den Artikel.</span><span class="sxs-lookup"><span data-stu-id="1d17f-112">Specified calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item.</span></span> <span data-ttu-id="1d17f-113">Als Berechnungsmenge wird zunächst die Standardauftragsmenge des Artikels verwendet, doch dieser Standardwert kann manuell außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1d17f-113">The calculation quantity initially uses the item’s standard order quantity, but the default value can be manually overridden.</span></span> <span data-ttu-id="1d17f-114">Die angegebene Berechnungsmenge stellt die Nachkalkulationslosgröße für den angegebenen Artikel und für hergestellte Komponenten mit dem Stücklistenpositionstyp "Produktion" dar.</span><span class="sxs-lookup"><span data-stu-id="1d17f-114">The specified calculation quantity represents the costing lot size for the specified item, and for manufactured components that have a BOM line type of production.</span></span> <span data-ttu-id="1d17f-115">Dies beruht auf der Annahme, dass die Komponente in der exakten Menge produziert wird.</span><span class="sxs-lookup"><span data-stu-id="1d17f-115">This is because it is assumed that the component will be produced to the exact quantity.</span></span> <span data-ttu-id="1d17f-116">Die Nachkalkulationslosgröße für andere produzierte Komponenten mit dem Stücklistenpositionstyp "Artikel" gibt deren jeweilige Standardauftragsmenge wieder.</span><span class="sxs-lookup"><span data-stu-id="1d17f-116">The costing lot size for other manufactured components that have a BOM line type of item will reflect their standard order quantity.</span></span>
-   <span data-ttu-id="1d17f-117">Angegebene Berechnungsmenge vom Typ "Auf Auftrag fertigen" in der Herstellkostenkalkulation eines Artikels − Die angegebene Berechnungsmenge fungiert als Nachkalkulationslosgröße für den Artikel und dessen produzierte Komponenten, wenn in einer Herstellkostenkalkulation der Stücklistenauflösungsmodus "Auf Auftrag fertigen" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1d17f-117">Specified make-to-order calculation quantity in an item’s BOM calculation − The specified calculation quantity acts as the costing lot size for the item and its manufactured components when BOM calculations use a make-to-order explosion mode.</span></span> <span data-ttu-id="1d17f-118">Es wird angenommen, dass die produzierten Komponenten – ebenso wie beim Stücklistenpositionstyp "Produktion" – in der exakten Menge produziert werden.</span><span class="sxs-lookup"><span data-stu-id="1d17f-118">It is assumed that the manufactured components will be produced to the exact quantity, just like a manufactured component that has a BOM line type of production.</span></span>
-   <span data-ttu-id="1d17f-119">Angegebene Berechnungsmenge in einer auftragsspezifischen Herstellkostenkalkulation − Eine auftragsspezifische Herstellkostenkalkulation kann für den Positionsartikel eines Auftrags, eines Verkaufsangebots oder eines Serviceauftrags ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1d17f-119">Specified calculation quantity in an order-specific BOM calculation − An order-specific BOM calculation can be performed for a line item on a sales order, sales quotation, or service order.</span></span> <span data-ttu-id="1d17f-120">Für die angegebene Berechnungsmenge wird standardmäßig auf die Menge des ursprünglichen Positionsartikels verwendet, diese Standardmenge kann jedoch außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="1d17f-120">The specified calculation quantity uses the quantity on the originating line item, but the default quantity can be overridden.</span></span> <span data-ttu-id="1d17f-121">Sie können wählen, ob für die auftragsspezifische Herstellkostenkalkulation der Stücklistenauflösungsmodus "Auf Auftrag fertigen" oder der Stücklistenauflösungsmodus "Mehrere Ebenen" verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1d17f-121">You can select whether the order-specific BOM calculation uses a make-to-order or multilevel explosion mode.</span></span>

<span data-ttu-id="1d17f-122">Der berechnete Betrag der amortisierten konstanten Kosten eines produzierten Artikels wird als Belastungen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="1d17f-122">The calculated amount of a manufactured item’s amortized constant costs is termed charges.</span></span>






