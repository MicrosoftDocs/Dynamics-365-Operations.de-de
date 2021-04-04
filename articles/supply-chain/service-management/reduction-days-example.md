---
title: Minderungstage – Beispiel
description: Minderungstage – Beispiel.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: df528bf7e95ee7ea74a792894b5e1c2f50c57730
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234752"
---
# <a name="reduction-days-example"></a><span data-ttu-id="ccf94-103">Minderungstage – Beispiel</span><span class="sxs-lookup"><span data-stu-id="ccf94-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="ccf94-104">Sie haben eine Dauerauftragsbuchung für den Wartungsdauerauftrag eines Debitors erstellt und dabei die in der folgenden Tabelle aufgeführten Werte verwendet:</span><span class="sxs-lookup"><span data-stu-id="ccf94-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="ccf94-105">Von Datum</span><span class="sxs-lookup"><span data-stu-id="ccf94-105">From date</span></span></p></th>
<th><p><span data-ttu-id="ccf94-106">Bis Datum</span><span class="sxs-lookup"><span data-stu-id="ccf94-106">To date</span></span></p></th>
<th><p><span data-ttu-id="ccf94-107">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="ccf94-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="ccf94-108">Dauerauftragstyp</span><span class="sxs-lookup"><span data-stu-id="ccf94-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="ccf94-109">Projekt</span><span class="sxs-lookup"><span data-stu-id="ccf94-109">Project</span></span></p></th>
<th><p><span data-ttu-id="ccf94-110">Kategorie</span><span class="sxs-lookup"><span data-stu-id="ccf94-110">Category</span></span></p></th>
<th><p><span data-ttu-id="ccf94-111">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="ccf94-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="ccf94-112">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="ccf94-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccf94-113">01. März 2011</span><span class="sxs-lookup"><span data-stu-id="ccf94-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="ccf94-114">31. März 2011</span><span class="sxs-lookup"><span data-stu-id="ccf94-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="ccf94-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="ccf94-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="ccf94-116"><strong>Regelmäßig</strong></span><span class="sxs-lookup"><span data-stu-id="ccf94-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="ccf94-117">9013</span><span class="sxs-lookup"><span data-stu-id="ccf94-117">9013</span></span></p></td>
<td><p><span data-ttu-id="ccf94-118">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="ccf94-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="ccf94-119">EUR</span><span class="sxs-lookup"><span data-stu-id="ccf94-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="ccf94-120">200,00</span><span class="sxs-lookup"><span data-stu-id="ccf94-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccf94-121">Der Debitor teilt Ihnen mit, dass er an zwei Tagen (10. und 11. März) keine Dienstleistungen in Anspruch nehmen will.</span><span class="sxs-lookup"><span data-stu-id="ccf94-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="ccf94-122">Sie vereinbaren, den Dauerauftrag um diese beiden Tage zu verkürzen.</span><span class="sxs-lookup"><span data-stu-id="ccf94-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="ccf94-123">Sie erstellen eine neue Buchung vom Typ **Minderungstage** gemäß der folgenden Tabelle:</span><span class="sxs-lookup"><span data-stu-id="ccf94-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="ccf94-124">Anfangsdatum</span><span class="sxs-lookup"><span data-stu-id="ccf94-124">From date</span></span></p></th>
<th><p><span data-ttu-id="ccf94-125">Enddatum</span><span class="sxs-lookup"><span data-stu-id="ccf94-125">To date</span></span></p></th>
<th><p><span data-ttu-id="ccf94-126">Dauerauftrag</span><span class="sxs-lookup"><span data-stu-id="ccf94-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="ccf94-127">Dauerauftragstyp</span><span class="sxs-lookup"><span data-stu-id="ccf94-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="ccf94-128">Projekt</span><span class="sxs-lookup"><span data-stu-id="ccf94-128">Project</span></span></p></th>
<th><p><span data-ttu-id="ccf94-129">Kategorie</span><span class="sxs-lookup"><span data-stu-id="ccf94-129">Category</span></span></p></th>
<th><p><span data-ttu-id="ccf94-130">Verkaufswährung</span><span class="sxs-lookup"><span data-stu-id="ccf94-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="ccf94-131">Verkaufspreis</span><span class="sxs-lookup"><span data-stu-id="ccf94-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ccf94-132">10. März 2011</span><span class="sxs-lookup"><span data-stu-id="ccf94-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="ccf94-133">11. März 2011</span><span class="sxs-lookup"><span data-stu-id="ccf94-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="ccf94-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="ccf94-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="ccf94-135"><strong>Minderungstage</strong></span><span class="sxs-lookup"><span data-stu-id="ccf94-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="ccf94-136">9013</span><span class="sxs-lookup"><span data-stu-id="ccf94-136">9013</span></span></p></td>
<td><p><span data-ttu-id="ccf94-137">UnterKat2</span><span class="sxs-lookup"><span data-stu-id="ccf94-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="ccf94-138">EUR</span><span class="sxs-lookup"><span data-stu-id="ccf94-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="ccf94-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="ccf94-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ccf94-140">Bei der Fakturierung der Buchungen für März 2011 wird der Verkaufspreis von EUR 200 um EUR 12,90 verringert.</span><span class="sxs-lookup"><span data-stu-id="ccf94-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="ccf94-141">Der fakturierbare Betrag für die Dauerauftragsbuchung beträgt somit EUR 187,10, und es werden zwei Buchungen mit einem Gesamtwert von EUR 187,10 fakturiert.</span><span class="sxs-lookup"><span data-stu-id="ccf94-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="ccf94-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ccf94-142">See also</span></span>

[<span data-ttu-id="ccf94-143">Verringern der Tage für Dauerauftragsgebühren</span><span class="sxs-lookup"><span data-stu-id="ccf94-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]