---
title: Preisregulierungen und Rabatte
description: Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Commerce.
author: scott-tucker
ms.date: 06/11/2021
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
ms.openlocfilehash: 44c03ae0a04d648e788a72d8f6dcc3671c5736c7
ms.sourcegitcommit: 7c9d6be464db058511df9cb6ba162d21dc0554e8
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2021
ms.locfileid: "6240941"
---
# <a name="price-adjustments-and-discounts"></a><span data-ttu-id="dda3b-103">Preisregulierungen und Rabatte</span><span class="sxs-lookup"><span data-stu-id="dda3b-103">Price adjustments and discounts</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="dda3b-104">Dieser Artikel enthält Informationen über Preisanpassungen und Rabatte in Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="dda3b-104">This article provides information about price adjustments and discounts in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="dda3b-105">Sie können in Commerce Preisregulierungen an Produkten vornehmen und zudem Rabatte einrichten, die auf einen Positionsartikel oder eine Transaktion in der Verkaufsstelle (POS), in einem Callcenterauftrag oder einem Onlineauftrag angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dda3b-105">In Commerce, you can make price adjustments to products, and can also set up discounts that are applied to a line item or a transaction at the point of sale (POS), in a call center sales order, or in an online order.</span></span> <span data-ttu-id="dda3b-106">Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="dda3b-106">Both price adjustments and discounts can be linked to price groups.</span></span> <span data-ttu-id="dda3b-107">Für sowohl Preisregulierungen als auch Rabatte können Sie ein einzelnes Start- und Enddatum bzw. einen Wiederholungszeitraum, einen Rabattcode und einige weitere Attribute angeben.</span><span class="sxs-lookup"><span data-stu-id="dda3b-107">For both price adjustments and discounts, you can specify a single start date and end date or a reoccurring period, a discount code, and a few additional attributes.</span></span> 

<span data-ttu-id="dda3b-108">Preisregulierungen und Rabatte können auf Produkte, Varianten oder Kategorien angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="dda3b-108">Price adjustments and discounts can be applied to products, variants, or categories.</span></span> <span data-ttu-id="dda3b-109">Entspricht mehr als ein Rabatt einem Produkt, erhält ein Debitor möglicherweise entweder einen der Rabatte oder einen kombinierten Rabatt, abhängig von der Konfiguration des Rabatts.</span><span class="sxs-lookup"><span data-stu-id="dda3b-109">If more than one discount applies to a product, a customer might receive either one of the discounts or a combined discount, depending on the configuration of the discount.</span></span> <span data-ttu-id="dda3b-110">Commerce übernimmt automatisch den Rabatt oder die Kombination von Rabatten, die dem Kunden den besten Preis ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="dda3b-110">Commerce automatically applies the discount or combination of discounts that gives the best price to the customer.</span></span> <span data-ttu-id="dda3b-111">Wenn Sie eine Preisregulierung oder einen Rabatt einrichten, sollten Sie sich vergewissern, dass Sie bestätigen, dass Preisgruppen den richtigen Kanälen, Katalogen, Zuordnungen oder Treueprogrammen zugeordnet sind, für die der Rabatt gelten soll.</span><span class="sxs-lookup"><span data-stu-id="dda3b-111">When you set up a price adjustment or a discount, be sure to confirm that price groups are assigned to the correct channels, catalogs, affiliations, or loyalty programs that you want the discount to apply to.</span></span> <span data-ttu-id="dda3b-112">Auch wenn Sie die Rabattkennung automatisch generieren möchten, können Sie Nummernkreise auf der Seite **Commerce Parameter** einrichten, bevor Sie einen neuen Rabatt oder eine Preisregulierung definieren.</span><span class="sxs-lookup"><span data-stu-id="dda3b-112">Additionally, if you want to automatically generate the discount ID, set up number sequences on the **Commerce parameters** page before you define a new price adjustment or discount.</span></span>

> [!NOTE]
> <span data-ttu-id="dda3b-113">Sie können eine Preisregulierung oder einen Rabatt löschen.</span><span class="sxs-lookup"><span data-stu-id="dda3b-113">You can delete a price adjustment or a discount.</span></span> <span data-ttu-id="dda3b-114">Allerdings gehen statistische Daten verloren.</span><span class="sxs-lookup"><span data-stu-id="dda3b-114">However, statistical information will be lost.</span></span>

## <a name="types-of-discounts"></a><span data-ttu-id="dda3b-115">Rabatttypen</span><span class="sxs-lookup"><span data-stu-id="dda3b-115">Types of discounts</span></span>

<span data-ttu-id="dda3b-116">Es gibt viele verschiedene Arten von Rabatten:</span><span class="sxs-lookup"><span data-stu-id="dda3b-116">There are many types of discounts:</span></span>

- <span data-ttu-id="dda3b-117">**Einfacher Rabatt** - ein einzelner Prozentsatz oder ein Betrag.</span><span class="sxs-lookup"><span data-stu-id="dda3b-117">**Simple discount** – A single percentage or amount.</span></span>
- <span data-ttu-id="dda3b-118">**Mengenrabatt** – Ein Rabatt, der bei Kauf von zwei oder mehr Produkten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dda3b-118">**Quantity discount** – A discount that is applied when two or more products are purchased.</span></span>
- <span data-ttu-id="dda3b-119">**Rabatt für Angebots-Sortiment** – Ein Rabatt, der beim Kauf einer bestimmten Kombination von Produkten angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="dda3b-119">**Mix and match discount** – A discount that is applied when a specific combination of products is purchased.</span></span>
- <span data-ttu-id="dda3b-120">**Schwellenwertrabatt** – Ein Rabatt, der angewendet wird, wenn die Summe der Buchung höher als ein angegebener Betrag ist.</span><span class="sxs-lookup"><span data-stu-id="dda3b-120">**Threshold discount** – A discount that is applied when the transaction total is more than a specified amount.</span></span>
- <span data-ttu-id="dda3b-121">**Zahlungsmittelbasierter Rabatt** – Ein Rabatt, der angewendet wird, wenn der Transaktionsbetrag einen angegebenen Betrag überschreitet und eine bestimmte Zahlungsart (z. B. Bargeld, Kredit- oder Debitkarte) zur Zahlung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dda3b-121">**Tender-based discount** – A discount that is applied when the transaction total is more than a specified amount and a specific payment type (for example, cash, credit, or debit card) is used for payment.</span></span>
- <span data-ttu-id="dda3b-122">**Lieferrabatt** – Ein Rabatt, der angewendet wird, wenn der Gesamtbetrag der Transaktion einen angegebenen Betrag übersteigt und eine bestimmte Lieferart (z. B. Lieferung in zwei Tagen oder Lieferung über Nacht) beim Auftrag verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dda3b-122">**Shipping discount** – A discount that is applied when the transaction total is more than a specified amount and a specific mode of delivery (for example, two day shipping or overnight shipping) is used on the order.</span></span>

<span data-ttu-id="dda3b-123">Sowohl Preisregulierungen als auch Rabatte können mit Preisgruppen verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="dda3b-123">Both price adjustments and discounts can be associated with price groups.</span></span> <span data-ttu-id="dda3b-124">Preisgruppen können anschließend Kanälen, Katalogen, Zuordnungen und Treueprogrammen zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="dda3b-124">Price groups can then be associated with channels, catalogs, affiliations, and loyalty programs.</span></span>

> [!NOTE]
> <span data-ttu-id="dda3b-125">Der Mix-and-Match-Rabatt und der Schwellenrabatt haben die Eigenschaften „Nicht rabattfähige Produkte zählen“ bzw. „Nicht rabattierbare Produkte auf den Schwellenwert anrechnen“.</span><span class="sxs-lookup"><span data-stu-id="dda3b-125">The mix and match discount and the threshold discount have properties named "Count non-discountable products" and "Count non-discountable products towards threshold", respectively.</span></span> <span data-ttu-id="dda3b-126">Wenn diese Eigenschaften aktiviert sind, kann ein Artikel, für den kein Rabatt in Frage kommt, dennoch dazu beitragen, eine Transaktion für den Rabatt zu qualifizieren, aber der nicht rabattfähige Artikel erhält keinen Rabatt.</span><span class="sxs-lookup"><span data-stu-id="dda3b-126">If these properties are enabled, an item that is not eligible for any discount can still help qualify a transaction for the discount, but the ineligible item will not get the discount.</span></span> 
> 
> <span data-ttu-id="dda3b-127">Wenn Sie beispielsweise einen Mix-and-Match-Rabatt mit zwei Zeilen A und B erstellen, bei dem ein Kunde 10 % Rabatt auf beide Artikel erhalten soll, aber Artikel A die Konfiguration „Alle Rabatte verhindern“ aktiviert hat, dann würde dies normalerweise den Artikel stoppen A von der Ermäßigung ab.</span><span class="sxs-lookup"><span data-stu-id="dda3b-127">For example, if you create a mix and match discount with two lines, A and B, where a customer should get 10% off on both items, but item A has the configuration "Prevent all discounts" checked, then this would typically stop item A from being included in the discount.</span></span> <span data-ttu-id="dda3b-128">Wenn jedoch die Eigenschaft „Nicht rabattierbare Produkte zählen“ aktiviert ist, kann Artikel A verwendet werden, um sich für den Mix-and-Match-Rabatt zu qualifizieren, aber der Rabatt von 10 % wird nur auf Artikel B angewendet. Eine ähnliche Logik gilt für den Schwellenrabatt.</span><span class="sxs-lookup"><span data-stu-id="dda3b-128">However, if the "Count non-discountable products" property is enabled, then item A can be used to qualify for the mix and match discount, but the 10% discount will only be applied to item B. Similar logic applies to the threshold discount.</span></span> 
>
> <span data-ttu-id="dda3b-129">Die Eigenschaft „Nicht rabattfähige Produkte zum Schwellenwert zählen“ hat jedoch eine zusätzliche Funktion im Vergleich zur Eigenschaft „Nicht rabattierbare Produkte zählen“ der Mix-and-Match-Rabatte.</span><span class="sxs-lookup"><span data-stu-id="dda3b-129">However, the property "Count non-discountable products towards threshold" has an additional capability when compared to the "Count non-discountable products" property of the mix and match discounts.</span></span> <span data-ttu-id="dda3b-130">Wenn der Schwellenrabatt aktiviert ist und es für einen Artikel einen bestehenden Rabatt gibt, der den Artikel von anderen Rabatten abhalten würde, würde der für diesen Artikel bezahlte Preis den Schwellenwert erreichen, aber dieser Artikel erhält keine zusätzlichen Rabatte.</span><span class="sxs-lookup"><span data-stu-id="dda3b-130">If the threshold discount is enabled, and if there is an item that has an existing discount which would prevent the item from any other discounts, then  the price paid for this item would qualify towards meeting the threshold, but this item will not get the additional discount.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
