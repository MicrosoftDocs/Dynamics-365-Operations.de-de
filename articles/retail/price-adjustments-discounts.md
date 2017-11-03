---
title: Preisregulierungen und Rabatte
description: "Dieser Artikel enthält Informationen zu Preisregulierungen und Rabatten für Microsoft Dynamics 365 for Retail."
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 9220cc12abf7134d425e088939d20ea03239a75a
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="f38a8-103">Preisregulierungen und Rabatte</span><span class="sxs-lookup"><span data-stu-id="f38a8-103">Price adjustments and discounts</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="f38a8-104">Dieser Artikel enthält Informationen zu Preisregulierungen und Rabatten für Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="f38a8-104">This article provides information about price adjustments and discounts in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="f38a8-105">Im Dynamics 365 for Retail können Sie Preisregulierungen an Produkten vornehmen und Rabatte einrichten, die einem Artikel oder einer Buchung einer Verkaufsstelle (POS), in einem Callcenterauftrag oder in einer Onlinebestellung angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f38a8-105">In Dynamics 365 for Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="f38a8-106">Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="f38a8-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="f38a8-107">Für sowohl Preisregulierungen als auch Rabatte können Sie ein einzelnes Start- und Enddatum bzw. einen Wiederholungszeitraum, einen Rabattcode und einige weitere Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="f38a8-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="f38a8-108">Preisregulierungen und Rabatte können auf Produkte, Varianten oder Kategorien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="f38a8-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="f38a8-109">Entspricht mehr als ein Rabatt einem Produkt, erhält ein Debitor möglicherweise entweder einen der Rabatte oder einen kombinierten Rabatt, abhängig von der Konfiguration des Rabatts.</span><span class="sxs-lookup"><span data-stu-id="f38a8-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="f38a8-110">Dynamics 365 for Retail übernimmt automatisch den Rabatt oder die Kombination von Rabatten, die dem Debitor den besten Preis ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f38a8-110">Dynamics 365 for Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="f38a8-111">Wenn Sie eine Preisregulierung oder einen Rabatt einrichten, sollten Sie sich vergewissern, dass Sie bestätigen, dass Preisgruppen den richtigen Kanälen, Katalogen, Zuordnungen oder Treueprogrammen zugeordnet sind, für die der Rabatt gelten soll.</span><span class="sxs-lookup"><span data-stu-id="f38a8-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="f38a8-112">Auch wenn Sie die Rabattkennung automatisch generieren möchten, können Sie Nummernkreise auf der Seite **Einzelhandelsparameter** einrichten, bevor Sie einen neuen Rabatt oder eine Preisregulierung definieren.</span><span class="sxs-lookup"><span data-stu-id="f38a8-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span> <span data-ttu-id="f38a8-113">**Hinweis:** Sie können eine Preisregulierung oder einen Rabatt löschen.</span><span class="sxs-lookup"><span data-stu-id="f38a8-113">**Note:** You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="f38a8-114">Allerdings gehen statistische Daten verloren.</span><span class="sxs-lookup"><span data-stu-id="f38a8-114">However, statistical information will be lost.</span></span>

### <a name="types-of-discounts"></a><span data-ttu-id="f38a8-115">Rabatttypen</span><span class="sxs-lookup"><span data-stu-id="f38a8-115">Types of discounts</span></span>

<span data-ttu-id="f38a8-116">Es gibt vier Arten von Einzelhandelsrabatten:</span><span class="sxs-lookup"><span data-stu-id="f38a8-116">There are four types of retail discounts:</span></span>

-   <span data-ttu-id="f38a8-117">**Einfacher Rabatt** - ein einzelner Prozentsatz oder ein Betrag.</span><span class="sxs-lookup"><span data-stu-id="f38a8-117">**Simple discount** – A single percentage or amount.</span></span>
-   <span data-ttu-id="f38a8-118">**Mengenrabatt** – Ein Rabatt, der bei Kauf von zwei oder mehr Produkten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f38a8-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
-   <span data-ttu-id="f38a8-119">**Rabatt für Angebots-Sortiment** – Ein Rabatt, der beim Kauf einer bestimmten Kombination von Produkten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="f38a8-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
-   <span data-ttu-id="f38a8-120">**Schwellenwertrabatt** – Ein Rabatt, der angewendet wird, wenn die Summe der Buchung höher als ein angegebener Betrag ist.</span><span class="sxs-lookup"><span data-stu-id="f38a8-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="f38a8-121">Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="f38a8-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="f38a8-122">Preisgruppen können anschließend Kanälen, Katalogen, Zuordnungen und Treueprogrammen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f38a8-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>




