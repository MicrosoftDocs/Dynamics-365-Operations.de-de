---
title: Preisregulierungen und Rabatte
description: Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Commerce.
author: scott-tucker
ms.date: 11/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RetailParameters, RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.custom: 15891
ms.assetid: bab5adf3-ddf0-4c22-a2eb-b4d25b88de99
ms.search.region: global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 2d3e8025c5ab28296713634094694156f9addf62
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802790"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="3924b-103">Preisregulierungen und Rabatte</span><span class="sxs-lookup"><span data-stu-id="3924b-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3924b-104">Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3924b-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3924b-105">Sie können in Commerce Preisregulierungen an Produkten vornehmen und zudem Rabatte einrichten, die auf einen Positionsartikel oder eine Transaktion in der Verkaufsstelle (POS), in einem Callcenterauftrag oder einem Onlineauftrag angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3924b-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="3924b-106">Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="3924b-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="3924b-107">Für sowohl Preisregulierungen als auch Rabatte können Sie ein einzelnes Start- und Enddatum bzw. einen Wiederholungszeitraum, einen Rabattcode und einige weitere Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="3924b-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="3924b-108">Preisregulierungen und Rabatte können auf Produkte, Varianten oder Kategorien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="3924b-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="3924b-109">Entspricht mehr als ein Rabatt einem Produkt, erhält ein Debitor möglicherweise entweder einen der Rabatte oder einen kombinierten Rabatt, abhängig von der Konfiguration des Rabatts.</span><span class="sxs-lookup"><span data-stu-id="3924b-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="3924b-110">Commerce übernimmt automatisch den Rabatt oder die Kombination von Rabatten, die dem Kunden den besten Preis ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="3924b-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="3924b-111">Wenn Sie eine Preisregulierung oder einen Rabatt einrichten, sollten Sie sich vergewissern, dass Sie bestätigen, dass Preisgruppen den richtigen Kanälen, Katalogen, Zuordnungen oder Treueprogrammen zugeordnet sind, für die der Rabatt gelten soll.</span><span class="sxs-lookup"><span data-stu-id="3924b-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="3924b-112">Auch wenn Sie die Rabattkennung automatisch generieren möchten, können Sie Nummernkreise auf der Seite **Commerce Parameter** einrichten, bevor Sie einen neuen Rabatt oder eine Preisregulierung definieren.</span><span class="sxs-lookup"><span data-stu-id="3924b-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="3924b-113">Sie können eine Preisregulierung oder einen Rabatt löschen.</span><span class="sxs-lookup"><span data-stu-id="3924b-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="3924b-114">Allerdings gehen statistische Daten verloren.</span><span class="sxs-lookup"><span data-stu-id="3924b-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="3924b-115">Rabatttypen</span><span class="sxs-lookup"><span data-stu-id="3924b-115">Types of discounts</span></span>

<span data-ttu-id="3924b-116">Es gibt viele verschiedene Arten von Rabatten:</span><span class="sxs-lookup"><span data-stu-id="3924b-116">There are many types of discounts:</span></span>

- <span data-ttu-id="3924b-117">**Einfacher Rabatt** - ein einzelner Prozentsatz oder ein Betrag.</span><span class="sxs-lookup"><span data-stu-id="3924b-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="3924b-118">**Mengenrabatt** – Ein Rabatt, der bei Kauf von zwei oder mehr Produkten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3924b-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="3924b-119">**Rabatt für Angebots-Sortiment** – Ein Rabatt, der beim Kauf einer bestimmten Kombination von Produkten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="3924b-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="3924b-120">**Schwellenwertrabatt** – Ein Rabatt, der angewendet wird, wenn die Summe der Buchung höher als ein angegebener Betrag ist.</span><span class="sxs-lookup"><span data-stu-id="3924b-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="3924b-121">**Zahlungsmittelbasierter Rabatt** – Ein Rabatt, der angewendet wird, wenn der Transaktionsbetrag einen angegebenen Betrag überschreitet und eine bestimmte Zahlungsart (z. B. Bargeld, Kredit- oder Debitkarte) zur Zahlung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3924b-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="3924b-122">**Lieferrabatt** – Ein Rabatt, der angewendet wird, wenn der Gesamtbetrag der Transaktion einen angegebenen Betrag übersteigt und eine bestimmte Lieferart (z. B. Lieferung in zwei Tagen oder Lieferung über Nacht) beim Auftrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3924b-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="3924b-123">Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="3924b-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="3924b-124">Preisgruppen können anschließend Kanälen, Katalogen, Zuordnungen und Treueprogrammen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="3924b-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]