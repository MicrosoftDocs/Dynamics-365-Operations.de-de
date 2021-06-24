---
title: Lieferzeitpläne
description: Lieferzeitpläne ermöglichen Ihnen, Auftragspositionsmengen zu verfolgen, wenn Sie mehrere Lieferungen für einen einzelnen Auftrag, ein Verkaufsangebot oder eine Bestellung verwenden.
author: ShylaThompson
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: kamaybac
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3dbd66d499b5d5f9f8ef21c0ce3752031a5f4672
ms.sourcegitcommit: 74e47075eab2b0b28f82b0d57f439719847ecb01
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/07/2021
ms.locfileid: "6193781"
---
# <a name="delivery-schedules"></a><span data-ttu-id="8052a-103">Lieferzeitpläne</span><span class="sxs-lookup"><span data-stu-id="8052a-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8052a-104">Lieferzeitpläne ermöglichen Ihnen, Auftragspositionsmengen zu verfolgen, wenn Sie mehrere Lieferungen für einen einzelnen Auftrag, ein Verkaufsangebot oder eine Bestellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="8052a-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="8052a-105">Ein Lieferzeitplan wird verwendet, wenn eine Gesamtmenge für einen Auftrag oder ein Angebot angefordert wird, um in mehreren Lieferungen geliefert zu werden.</span><span class="sxs-lookup"><span data-stu-id="8052a-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="8052a-106">Einzelne Sendungen werden von Lieferpositionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8052a-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="8052a-107">Zwei oder mehr Lieferpositionen bilden einen Lieferzeitplan.</span><span class="sxs-lookup"><span data-stu-id="8052a-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="8052a-108">Die Lieferpositionen können verschiedene Lieferdaten, Mengen, Lieferarten und Lagerdimensionen haben, wie Standort und Lagerort.</span><span class="sxs-lookup"><span data-stu-id="8052a-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="8052a-109">**Beispiel zum Löschen eines gesamten Lieferzeitplans**</span><span class="sxs-lookup"><span data-stu-id="8052a-109">**Example of a delivery schedule**</span></span>

| <span data-ttu-id="8052a-110">Artikel</span><span class="sxs-lookup"><span data-stu-id="8052a-110">Item</span></span>                              | <span data-ttu-id="8052a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="8052a-111">Value</span></span>                                    |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="8052a-112">Gesamte Bestellung (ursprüngliche Auftragsposition)</span><span class="sxs-lookup"><span data-stu-id="8052a-112">Total order (original order line)</span></span> | <span data-ttu-id="8052a-113">600 Stühle</span><span class="sxs-lookup"><span data-stu-id="8052a-113">600 chairs</span></span>                               |
| <span data-ttu-id="8052a-114">Angeforderter Lieferzeitplan</span><span class="sxs-lookup"><span data-stu-id="8052a-114">Requested delivery schedule</span></span>       | <span data-ttu-id="8052a-115">100 Stühle pro Monat</span><span class="sxs-lookup"><span data-stu-id="8052a-115">100 chairs per month</span></span>                     |
| <span data-ttu-id="8052a-116">Angeforderter Lieferzeitrahmen</span><span class="sxs-lookup"><span data-stu-id="8052a-116">Requested time frame for delivery</span></span> | <span data-ttu-id="8052a-117">6 Monate, jeweils am 1 Tag jedes Monats</span><span class="sxs-lookup"><span data-stu-id="8052a-117">6 months, on the first day of each month</span></span> |

<span data-ttu-id="8052a-118">In diesem Szenario fordert der Debitor die Lieferung von 600 Stühlen in Chargen von 100 Stühlen über einen Zeitraum von sechs Monaten hinweg.</span><span class="sxs-lookup"><span data-stu-id="8052a-118">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="8052a-119">Um die Lieferungsanforderungen zu verfolgen, erstellen Sie einen Lieferzeitplan.</span><span class="sxs-lookup"><span data-stu-id="8052a-119">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="8052a-120">Erstellen Sie auf der Lieferzeitplan-Seite sechs separate Lieferpositionen.</span><span class="sxs-lookup"><span data-stu-id="8052a-120">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="8052a-121">Jede Lieferposition umfasst 100 Stühle und gibt das Lieferdatum für die jeweiligen 100 Stühle an.</span><span class="sxs-lookup"><span data-stu-id="8052a-121">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="8052a-122">In diesem Fall wird die erste Position sechs Monate hintereinander jeweils für den 1. des Monats versetzt.</span><span class="sxs-lookup"><span data-stu-id="8052a-122">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="8052a-123">Wenn Sie den Lieferzeitplan erstellt haben, wird der Typ der ursprünglichen Auftragsposition automatisch auf **Auftragsposition mit mehreren Lieferungen** geändert.</span><span class="sxs-lookup"><span data-stu-id="8052a-123">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="8052a-124">Eine Position dieses Typs verweist auf eine geschäftsbezogene Position und wird durch ein Symbol gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8052a-124">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="8052a-125">Die Lieferposition wird durch ein anderes Symbol gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="8052a-125">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="8052a-126">Wenn Sie eine Menge in einer Lieferposition ändern, wird die Position in der Gesamtmenge des Lieferzeitplans aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8052a-126">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="8052a-127">Falls eine Handelsvereinbarung mit einem definierten Gesamtauftragsrabatt besteht, wird mithilfe des Lieferzeitplans außerdem sichergestellt, dass der Gesamtauftragsrabatt auch dann für den Auftrag gilt, wenn dieser in einzelne Lieferungen unterteilt ist.</span><span class="sxs-lookup"><span data-stu-id="8052a-127">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="8052a-128">Aufträge, die einen Lieferzeitplan haben, werden mit den Lieferpositionen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8052a-128">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="8052a-129">Die Verarbeitung umfasst die Buchung von Lieferscheinen, Produktzugängen und die Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="8052a-129">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="8052a-130">Dokumentausdrucke von Aufträgen und Angeboten mit Lieferzeitplan zeigen nur die Lieferpositionen an.</span><span class="sxs-lookup"><span data-stu-id="8052a-130">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="8052a-131">Sie zeigen nicht die ursprünglichen Positionen an (geschäftsbezogene Positionen).</span><span class="sxs-lookup"><span data-stu-id="8052a-131">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="8052a-132">**Hinweis:** Außerdem werden die Lieferpositionen angezeigt, wenn Sie diese Aktivitäten ausführen:</span><span class="sxs-lookup"><span data-stu-id="8052a-132">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="8052a-133">Buchen</span><span class="sxs-lookup"><span data-stu-id="8052a-133">Post</span></span>
-   <span data-ttu-id="8052a-134">Seiten kopieren</span><span class="sxs-lookup"><span data-stu-id="8052a-134">Copy pages</span></span>
-   <span data-ttu-id="8052a-135">Durchsuchen von Listenseiten und Berichten</span><span class="sxs-lookup"><span data-stu-id="8052a-135">Browse list pages and reports</span></span>

<span data-ttu-id="8052a-136">Beim Bestätigen eines Verkaufsangebots zeigt der Auftrag den gesamte Lieferzeitplan Auftragsposition an – auch dann, wenn Auftragspositionen mehrere Lieferungen haben.</span><span class="sxs-lookup"><span data-stu-id="8052a-136">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="8052a-137">Außerdem wird der gesamte Lieferzeitplan in allen Haupseiten angezeigt, z. B. Aufträgen, Verkaufsangeboten und Bestellungen.</span><span class="sxs-lookup"><span data-stu-id="8052a-137">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]