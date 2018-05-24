---
title: "Minderungstage – Beispiel"
description: "Minderungstage – Beispiel."
author: YuyuScheller
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 69e4b1b0fe100b17e5b2c59be81604019347956f
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---


# <a name="reduction-days-example"></a><span data-ttu-id="500b4-103">Minderungstage – Beispiel</span><span class="sxs-lookup"><span data-stu-id="500b4-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="500b4-104">Sie haben eine Dauerauftragsbuchung für den Wartungsdauerauftrag eines Debitors erstellt und dabei die in der folgenden Tabelle aufgeführten Werte verwendet:</span><span class="sxs-lookup"><span data-stu-id="500b4-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="500b4-105">Von Datum</span><span class="sxs-lookup"><span data-stu-id="500b4-105">From date</span></span></p></th>
<th><p><span data-ttu-id="500b4-106">Bis Datum</span><span class="sxs-lookup"><span data-stu-id="500b4-106">To date</span></span></p></th>
<th><p><span data-ttu-id="500b4-107">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="500b4-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="500b4-108">Dauerauftragstyp</span><span class="sxs-lookup"><span data-stu-id="500b4-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="500b4-109">Projekt</span><span class="sxs-lookup"><span data-stu-id="500b4-109">Project</span></span></p></th>
<th><p><span data-ttu-id="500b4-110">Kategorie</span><span class="sxs-lookup"><span data-stu-id="500b4-110">Category</span></span></p></th>
<th><p><span data-ttu-id="500b4-111">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="500b4-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="500b4-112">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="500b4-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500b4-113">01. März 2011</span><span class="sxs-lookup"><span data-stu-id="500b4-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="500b4-114">31. März 2011</span><span class="sxs-lookup"><span data-stu-id="500b4-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="500b4-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="500b4-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="500b4-116"><strong>Regelmäßig</strong></span><span class="sxs-lookup"><span data-stu-id="500b4-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="500b4-117">9013</span><span class="sxs-lookup"><span data-stu-id="500b4-117">9013</span></span></p></td>
<td><p><span data-ttu-id="500b4-118">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="500b4-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="500b4-119">EUR</span><span class="sxs-lookup"><span data-stu-id="500b4-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="500b4-120">200,00</span><span class="sxs-lookup"><span data-stu-id="500b4-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500b4-121">Der Debitor teilt Ihnen mit, dass er an zwei Tagen (10. und 11. März) keine Dienstleistungen in Anspruch nehmen will.</span><span class="sxs-lookup"><span data-stu-id="500b4-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="500b4-122">Sie vereinbaren, den Dauerauftrag um diese beiden Tage zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="500b4-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="500b4-123">Sie erstellen eine neue Buchung vom Typ **Minderungstage** gemäß der folgenden Tabelle:</span><span class="sxs-lookup"><span data-stu-id="500b4-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="500b4-124">Anfangsdatum</span><span class="sxs-lookup"><span data-stu-id="500b4-124">From date</span></span></p></th>
<th><p><span data-ttu-id="500b4-125">Enddatum</span><span class="sxs-lookup"><span data-stu-id="500b4-125">To date</span></span></p></th>
<th><p><span data-ttu-id="500b4-126">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="500b4-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="500b4-127">Dauerauftragstyp</span><span class="sxs-lookup"><span data-stu-id="500b4-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="500b4-128">Projekt</span><span class="sxs-lookup"><span data-stu-id="500b4-128">Project</span></span></p></th>
<th><p><span data-ttu-id="500b4-129">Kategorie</span><span class="sxs-lookup"><span data-stu-id="500b4-129">Category</span></span></p></th>
<th><p><span data-ttu-id="500b4-130">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="500b4-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="500b4-131">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="500b4-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="500b4-132">10. März 2011</span><span class="sxs-lookup"><span data-stu-id="500b4-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="500b4-133">11. März 2011</span><span class="sxs-lookup"><span data-stu-id="500b4-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="500b4-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="500b4-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="500b4-135"><strong>Minderungstage</strong></span><span class="sxs-lookup"><span data-stu-id="500b4-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="500b4-136">9013</span><span class="sxs-lookup"><span data-stu-id="500b4-136">9013</span></span></p></td>
<td><p><span data-ttu-id="500b4-137">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="500b4-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="500b4-138">EUR</span><span class="sxs-lookup"><span data-stu-id="500b4-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="500b4-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="500b4-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="500b4-140">Bei der Fakturierung der Buchungen für März 2011 wird der Verkaufspreis von EUR 200 um EUR 12,90 verringert.</span><span class="sxs-lookup"><span data-stu-id="500b4-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="500b4-141">Der fakturierbare Betrag für die Dauerauftragsbuchung beträgt somit EUR 187,10, und es werden zwei Buchungen mit einem Gesamtwert von EUR 187,10 fakturiert.</span><span class="sxs-lookup"><span data-stu-id="500b4-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="500b4-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="500b4-142">See also</span></span>

[<span data-ttu-id="500b4-143">Verringern der Tage für Dauerauftragsgebühren</span><span class="sxs-lookup"><span data-stu-id="500b4-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  



