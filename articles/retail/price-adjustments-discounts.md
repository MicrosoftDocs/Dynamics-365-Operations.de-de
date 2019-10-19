---
title: Preisregulierungen und Rabatte
description: Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Retail.
author: scott-tucker
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
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
ms.openlocfilehash: 9461496cf5334ff0a25361b9b426cacc0aa1f88c
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025240"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="2b7db-103">Preisregulierungen und Rabatte</span><span class="sxs-lookup"><span data-stu-id="2b7db-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2b7db-104">Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="2b7db-104">This article provides information about price adjustments and discounts in Dynamics 365 Retail.</span></span>

<span data-ttu-id="2b7db-105">Sie können in Retail Preisregulierungen an Produkten vornehmen und zudem Rabatte einrichten, die auf einen Positionsartikel oder eine Transaktion in der Verkaufsstelle (POS), in einem Callcenterauftrag oder einem Onlineauftrag angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b7db-105">In Retail, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="2b7db-106">Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="2b7db-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="2b7db-107">Für sowohl Preisregulierungen als auch Rabatte können Sie ein einzelnes Start- und Enddatum bzw. einen Wiederholungszeitraum, einen Rabattcode und einige weitere Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="2b7db-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> <span data-ttu-id="2b7db-108">Preisregulierungen und Rabatte können auf Produkte, Varianten oder Kategorien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b7db-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="2b7db-109">Entspricht mehr als ein Rabatt einem Produkt, erhält ein Debitor möglicherweise entweder einen der Rabatte oder einen kombinierten Rabatt, abhängig von der Konfiguration des Rabatts.</span><span class="sxs-lookup"><span data-stu-id="2b7db-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="2b7db-110">Retail übernimmt automatisch den Rabatt oder die Kombination von Rabatten, die dem Kunden den besten Preis ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="2b7db-110">Retail automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="2b7db-111">Wenn Sie eine Preisregulierung oder einen Rabatt einrichten, sollten Sie sich vergewissern, dass Sie bestätigen, dass Preisgruppen den richtigen Kanälen, Katalogen, Zuordnungen oder Treueprogrammen zugeordnet sind, für die der Rabatt gelten soll.</span><span class="sxs-lookup"><span data-stu-id="2b7db-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="2b7db-112">Auch wenn Sie die Rabattkennung automatisch generieren möchten, können Sie Nummernkreise auf der Seite **Einzelhandelsparameter** einrichten, bevor Sie einen neuen Rabatt oder eine Preisregulierung definieren.</span><span class="sxs-lookup"><span data-stu-id="2b7db-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Retail parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="2b7db-113">Sie können eine Preisregulierung oder einen Rabatt löschen.</span><span class="sxs-lookup"><span data-stu-id="2b7db-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="2b7db-114">Allerdings gehen statistische Daten verloren.</span><span class="sxs-lookup"><span data-stu-id="2b7db-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="2b7db-115">Rabatttypen</span><span class="sxs-lookup"><span data-stu-id="2b7db-115">Types of discounts</span></span>

<span data-ttu-id="2b7db-116">Es gibt vier Arten von Einzelhandelsrabatten:</span><span class="sxs-lookup"><span data-stu-id="2b7db-116">There are four types of retail discounts:</span></span>

- <span data-ttu-id="2b7db-117">**Einfacher Rabatt** - ein einzelner Prozentsatz oder ein Betrag.</span><span class="sxs-lookup"><span data-stu-id="2b7db-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="2b7db-118">**Mengenrabatt** – Ein Rabatt, der bei Kauf von zwei oder mehr Produkten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b7db-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="2b7db-119">**Rabatt für Angebots-Sortiment** – Ein Rabatt, der beim Kauf einer bestimmten Kombination von Produkten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="2b7db-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="2b7db-120">**Schwellenwertrabatt** – Ein Rabatt, der angewendet wird, wenn die Summe der Buchung höher als ein angegebener Betrag ist.</span><span class="sxs-lookup"><span data-stu-id="2b7db-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>

<span data-ttu-id="2b7db-121">Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="2b7db-121">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="2b7db-122">Preisgruppen können anschließend Kanälen, Katalogen, Zuordnungen und Treueprogrammen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="2b7db-122">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>
