---
title: Lieferzeitpläne
description: Lieferzeitpläne ermöglichen Ihnen, Auftragspositionsmengen zu verfolgen, wenn Sie mehrere Lieferungen für einen einzelnen Auftrag, ein Verkaufsangebot oder eine Bestellung verwenden.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 068a881a7fa9b19198bd3ad22988465be49c1fa3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1555815"
---
# <a name="delivery-schedules"></a><span data-ttu-id="d770e-103">Lieferzeitpläne</span><span class="sxs-lookup"><span data-stu-id="d770e-103">Delivery schedules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d770e-104">Lieferzeitpläne ermöglichen Ihnen, Auftragspositionsmengen zu verfolgen, wenn Sie mehrere Lieferungen für einen einzelnen Auftrag, ein Verkaufsangebot oder eine Bestellung verwenden.</span><span class="sxs-lookup"><span data-stu-id="d770e-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="d770e-105">Ein Lieferzeitplan wird verwendet, wenn eine Gesamtmenge für einen Auftrag oder ein Angebot angefordert wird, um in mehreren Lieferungen geliefert zu werden.</span><span class="sxs-lookup"><span data-stu-id="d770e-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="d770e-106">Einzelne Sendungen werden von Lieferpositionen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d770e-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="d770e-107">Zwei oder mehr Lieferpositionen bilden einen Lieferzeitplan.</span><span class="sxs-lookup"><span data-stu-id="d770e-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="d770e-108">Die Lieferpositionen können verschiedene Lieferdaten, Mengen, Lieferarten und Lagerdimensionen haben, wie Standort und Lagerort.</span><span class="sxs-lookup"><span data-stu-id="d770e-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="d770e-109">**Beispiel zum Löschen eines gesamten Lieferzeitplans**</span><span class="sxs-lookup"><span data-stu-id="d770e-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="d770e-110">Gesamte Bestellung (ursprüngliche Auftragsposition)</span><span class="sxs-lookup"><span data-stu-id="d770e-110">Total order (original order line)</span></span> | <span data-ttu-id="d770e-111">600 Stühle</span><span class="sxs-lookup"><span data-stu-id="d770e-111">600 chairs</span></span>                               |
| <span data-ttu-id="d770e-112">Angeforderter Lieferzeitplan</span><span class="sxs-lookup"><span data-stu-id="d770e-112">Requested delivery schedule</span></span>       | <span data-ttu-id="d770e-113">100 Stühle pro Monat</span><span class="sxs-lookup"><span data-stu-id="d770e-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="d770e-114">Angeforderter Lieferzeitrahmen</span><span class="sxs-lookup"><span data-stu-id="d770e-114">Requested time frame for delivery</span></span> | <span data-ttu-id="d770e-115">6 Monate, jeweils am 1 Tag jedes Monats</span><span class="sxs-lookup"><span data-stu-id="d770e-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="d770e-116">In diesem Szenario fordert der Debitor die Lieferung von 600 Stühlen in Chargen von 100 Stühlen über einen Zeitraum von sechs Monaten hinweg.</span><span class="sxs-lookup"><span data-stu-id="d770e-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="d770e-117">Um die Lieferungsanforderungen zu verfolgen, erstellen Sie einen Lieferzeitplan.</span><span class="sxs-lookup"><span data-stu-id="d770e-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="d770e-118">Erstellen Sie auf der Lieferzeitplan-Seite sechs separate Lieferpositionen.</span><span class="sxs-lookup"><span data-stu-id="d770e-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="d770e-119">Jede Lieferposition umfasst 100 Stühle und gibt das Lieferdatum für die jeweiligen 100 Stühle an.</span><span class="sxs-lookup"><span data-stu-id="d770e-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="d770e-120">In diesem Fall wird die erste Position sechs Monate hintereinander jeweils für den 1. des Monats versetzt.</span><span class="sxs-lookup"><span data-stu-id="d770e-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="d770e-121">Wenn Sie den Lieferzeitplan erstellt haben, wird der Typ der ursprünglichen Auftragsposition automatisch auf **Auftragsposition mit mehreren Lieferungen** geändert.</span><span class="sxs-lookup"><span data-stu-id="d770e-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="d770e-122">Eine Position dieses Typs verweist auf eine geschäftsbezogene Position und wird durch ein Symbol gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d770e-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="d770e-123">Die Lieferposition wird durch ein anderes Symbol gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d770e-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="d770e-124">Wenn Sie eine Menge in einer Lieferposition ändern, wird die Position in der Gesamtmenge des Lieferzeitplans aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="d770e-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="d770e-125">Falls eine Handelsvereinbarung mit einem definierten Gesamtauftragsrabatt besteht, wird mithilfe des Lieferzeitplans außerdem sichergestellt, dass der Gesamtauftragsrabatt auch dann für den Auftrag gilt, wenn dieser in einzelne Lieferungen unterteilt ist.</span><span class="sxs-lookup"><span data-stu-id="d770e-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="d770e-126">Aufträge, die einen Lieferzeitplan haben, werden mit den Lieferpositionen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="d770e-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="d770e-127">Die Verarbeitung umfasst die Buchung von Lieferscheinen, Produktzugängen und die Rechnungsstellung.</span><span class="sxs-lookup"><span data-stu-id="d770e-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="d770e-128">Dokumentausdrucke von Aufträgen und Angeboten mit Lieferzeitplan zeigen nur die Lieferpositionen an.</span><span class="sxs-lookup"><span data-stu-id="d770e-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="d770e-129">Sie zeigen nicht die ursprünglichen Positionen an (geschäftsbezogene Positionen).</span><span class="sxs-lookup"><span data-stu-id="d770e-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="d770e-130">**Hinweis:** Außerdem werden die Lieferpositionen angezeigt, wenn Sie diese Aktivitäten ausführen:</span><span class="sxs-lookup"><span data-stu-id="d770e-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="d770e-131">Buchen</span><span class="sxs-lookup"><span data-stu-id="d770e-131">Post</span></span>
-   <span data-ttu-id="d770e-132">Seiten kopieren</span><span class="sxs-lookup"><span data-stu-id="d770e-132">Copy pages</span></span>
-   <span data-ttu-id="d770e-133">Durchsuchen von Listenseiten und Berichten</span><span class="sxs-lookup"><span data-stu-id="d770e-133">Browse list pages and reports</span></span>

<span data-ttu-id="d770e-134">Beim Bestätigen eines Verkaufsangebots zeigt der Auftrag den gesamte Lieferzeitplan Auftragsposition an – auch dann, wenn Auftragspositionen mehrere Lieferungen haben.</span><span class="sxs-lookup"><span data-stu-id="d770e-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="d770e-135">Außerdem wird der gesamte Lieferzeitplan in allen Haupseiten angezeigt, z. B. Aufträgen, Verkaufsangeboten und Bestellungen.</span><span class="sxs-lookup"><span data-stu-id="d770e-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>



