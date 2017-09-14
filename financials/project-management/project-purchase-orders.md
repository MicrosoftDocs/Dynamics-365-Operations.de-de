---
title: "Bestellungen für ein Projekt"
description: "In diesem Artikel werden die verschiedenen Methoden beschrieben, die Sie verwenden können, um Bestellungen für ein Projekt zu erstellen. Die Methode, die Sie verwenden, wird durch den Zweck der Bestellung, durch den Verbrauchszeitpunkt der eingekauften Artikel und dem Zeitpunkt der Fakturierung für ein Projekt bestimmt."
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 6dd2aa1ebc713287120106a9d1ec7dc15c24def9
ms.openlocfilehash: 985a57ae9fb116b1c4514b836b35c5da0f8838fd
ms.contentlocale: de-de
ms.lasthandoff: 09/14/2017

---

# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="c3c3c-104">Bestellungen für ein Projekt</span><span class="sxs-lookup"><span data-stu-id="c3c3c-104">Purchase orders for a project</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="c3c3c-105">In diesem Artikel werden die verschiedenen Methoden beschrieben, die Sie verwenden können, um Bestellungen für ein Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="c3c3c-106">Die Methode, die Sie verwenden, wird durch den Zweck der Bestellung, durch den Verbrauchszeitpunkt der eingekauften Artikel und dem Zeitpunkt der Fakturierung für ein Projekt bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="c3c3c-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise Editton, können Sie mehrere Methoden verwenden, um Bestellungen für ein Projekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-107">In Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="c3c3c-108">Die Methode, die Sie verwenden, wird durch den Zweck der Bestellung, durch den Verbrauchszeitpunkt der eingekauften Artikel oder dem Zeitpunkt der Fakturierung der eingekauften Artikel für ein Projekt bestimmt.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="c3c3c-109">Methoden zum Erstellen einer Bestellung</span><span class="sxs-lookup"><span data-stu-id="c3c3c-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="c3c3c-110">Im Projektverwaltungs- und Buchhaltungsmodul stehen die folgenden Methoden zum Erstellen einer Bestellung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="c3c3c-111">Der Zweck der Bestellung bestimmt, wann eine Bestellung verbraucht wird, und damit, wann ein Projekt mit Artikeln belastet wird.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3c3c-112">Methode</span><span class="sxs-lookup"><span data-stu-id="c3c3c-112">Method</span></span></th>
<th><span data-ttu-id="c3c3c-113">Verwendungszweck</span><span class="sxs-lookup"><span data-stu-id="c3c3c-113">Purpose</span></span></th>
<th><span data-ttu-id="c3c3c-114">Verbrauch von Artikeln</span><span class="sxs-lookup"><span data-stu-id="c3c3c-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c3c3c-115">Erstellen einer Bestellung direkt über ein Projekt.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="c3c3c-116">Verwenden Sie diese Methode, um Artikel von einem externen Kreditor für den Verbrauch in einem Projekt zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="c3c3c-117">Sie können die Bestellung auf zwei Arten erstellen:</span><span class="sxs-lookup"><span data-stu-id="c3c3c-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="c3c3c-118">Aus dem Projekt selbst:</span><span class="sxs-lookup"><span data-stu-id="c3c3c-118">From the project itself.</span></span> <span data-ttu-id="c3c3c-119">In diesem Fall wurde das Projekt für die Bestellung bereits definiert.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="c3c3c-120">Per Navigation zur Projektbestellung</span><span class="sxs-lookup"><span data-stu-id="c3c3c-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="c3c3c-121">Hierbei müssen Sie sowohl den Kreditor als auch das Projekt auswählen, für den bzw. das die Bestellung erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="c3c3c-122">Artikel werden verbraucht, wenn die Kreditorenrechnung aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c3c3c-123">Bestellung aus einem Auftrag erstellen  </span><span class="sxs-lookup"><span data-stu-id="c3c3c-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="c3c3c-124">Verwenden Sie diese Methode, wenn Sie einen Auftrag über eon Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="c3c3c-125">Artikel werden verbraucht, wenn die Rechnung für den Auftrag an den Debitor gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c3c3c-126">Bestellung aus einem Artikelbedarf erstellen  </span><span class="sxs-lookup"><span data-stu-id="c3c3c-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="c3c3c-127">Verwenden Sie diese Methode, wenn Sie einen Artikelbedarfs über ein Projekt erstellen.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="c3c3c-128">Artikel werden verbraucht, wenn der Lieferschein des Artikelbedarfs aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="c3c3c-129">Wenn die Kreditorenrechnung oder der Lieferschein aktualisiert wird, werden Sie aufgefordert, den Lieferschein für den Artikelbedarf zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c3c3c-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="c3c3c-130">Weitere Informationen finden Sie unter[Entgegennehmen eines Artikel in Bestellungsanforderung](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="c3c3c-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>


