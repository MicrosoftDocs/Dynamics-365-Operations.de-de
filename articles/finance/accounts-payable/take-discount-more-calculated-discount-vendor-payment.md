---
title: Für eine Kreditorenzahlung mehr als den berechneten Rabatt nehmen
description: Dieser Artikel führt Sie durch ein Szenario, in dem ein Skonto für einen Betrag übernommen wird, der höher als der ursprünglich auf der Rechnung verfügbare Rabatt ist Dieses Szenario kann eintreten, wenn eine Organisation eine Vereinbarung mit dem Kreditor getroffen hat, einen geringen Betrag zu zahlen als auf der Rechnung vermerkt.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom: 14281
ms.assetid: 7f0a4197-95dd-4969-ade9-154815cf659e
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2a56331f76867aeac0bad0912749d96f959513e0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5235884"
---
# <a name="take-more-than-the-calculated-discount-for-a-vendor-payment"></a><span data-ttu-id="41158-104">Für eine Kreditorenzahlung mehr als den berechneten Rabatt nehmen</span><span class="sxs-lookup"><span data-stu-id="41158-104">Take more than the calculated discount for a vendor payment</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="41158-105">Dieser Artikel führt Sie durch ein Szenario, in dem ein Skonto für einen Betrag übernommen wird, der höher als der ursprünglich auf der Rechnung verfügbare Rabatt ist</span><span class="sxs-lookup"><span data-stu-id="41158-105">This article walks you through a scenario where a cash discount is taken for an amount that is more than the discount that was originally available on the invoice.</span></span> <span data-ttu-id="41158-106">Dieses Szenario kann eintreten, wenn eine Organisation eine Vereinbarung mit dem Kreditor getroffen hat, einen geringen Betrag zu zahlen als auf der Rechnung vermerkt.</span><span class="sxs-lookup"><span data-stu-id="41158-106">This scenario might occur if an organization comes to an agreement with the vendor to pay a smaller amount on the invoice.</span></span> 

<span data-ttu-id="41158-107">Kreditor 3051 gibt Fabrikam ein Skonto von 4 Prozent, wenn eine Rechnung in sieben Tagen beglichen wird.</span><span class="sxs-lookup"><span data-stu-id="41158-107">Vendor 3051 gives Fabrikam a cash discount of 4 percent if an invoice is paid in seven days.</span></span> <span data-ttu-id="41158-108">Am 29. Juni gibt April eine Rechnung für 1.000,00 ein.</span><span class="sxs-lookup"><span data-stu-id="41158-108">On June 29, April enters an invoice for 1,000.00.</span></span> <span data-ttu-id="41158-109">Der Händler gewährt April einen Rabatt von 60,00 anstelle des standardmäßigen Rabatts von 40,00, der für die Rechnung verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="41158-109">The vendor lets April take a discount of 60.00 instead of the default discount of 40.00 that is available for the invoice.</span></span> <span data-ttu-id="41158-110">April erfasst eine einmalige Zahlung, indem er die Zahlungserfassung "Kreditoren" verwendet.</span><span class="sxs-lookup"><span data-stu-id="41158-110">April records a one-off payment by using the Accounts payable payment journal.</span></span> <span data-ttu-id="41158-111">Sie gibt den Kreditor für die Zahlung ein und öffnet anschließend die Seite **Buchungen ausgleichen**.</span><span class="sxs-lookup"><span data-stu-id="41158-111">She enters the vendor for the payment and then opens the **Settle transactions** page.</span></span> <span data-ttu-id="41158-112">Sie markiert die Rechnung und ändert den Wert im Feld **Skontobetrag** in **60,00**.</span><span class="sxs-lookup"><span data-stu-id="41158-112">She marks the invoice and changes the value in the **Cash discount amount** field to **60.00**.</span></span>

| <span data-ttu-id="41158-113">Markieren</span><span class="sxs-lookup"><span data-stu-id="41158-113">Mark</span></span>     | <span data-ttu-id="41158-114">Skonto verwenden</span><span class="sxs-lookup"><span data-stu-id="41158-114">Use cash discount</span></span> | <span data-ttu-id="41158-115">Beleg</span><span class="sxs-lookup"><span data-stu-id="41158-115">Voucher</span></span>   | <span data-ttu-id="41158-116">Konto</span><span class="sxs-lookup"><span data-stu-id="41158-116">Account</span></span> | <span data-ttu-id="41158-117">Datum</span><span class="sxs-lookup"><span data-stu-id="41158-117">Date</span></span>      | <span data-ttu-id="41158-118">Fälligkeitsdatum</span><span class="sxs-lookup"><span data-stu-id="41158-118">Due date</span></span>  | <span data-ttu-id="41158-119">Rechnung</span><span class="sxs-lookup"><span data-stu-id="41158-119">Invoice</span></span> | <span data-ttu-id="41158-120">Betrag in Buchungswährung</span><span class="sxs-lookup"><span data-stu-id="41158-120">Amount in transaction currency</span></span> | <span data-ttu-id="41158-121">Währung</span><span class="sxs-lookup"><span data-stu-id="41158-121">Currency</span></span> | <span data-ttu-id="41158-122">Auszugleichender Betrag</span><span class="sxs-lookup"><span data-stu-id="41158-122">Amount to settle</span></span> |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| <span data-ttu-id="41158-123">Ausgewählt</span><span class="sxs-lookup"><span data-stu-id="41158-123">Selected</span></span> | <span data-ttu-id="41158-124">Normal</span><span class="sxs-lookup"><span data-stu-id="41158-124">Normal</span></span>            | <span data-ttu-id="41158-125">Inv-10040</span><span class="sxs-lookup"><span data-stu-id="41158-125">Inv-10040</span></span> | <span data-ttu-id="41158-126">3051</span><span class="sxs-lookup"><span data-stu-id="41158-126">3051</span></span>    | <span data-ttu-id="41158-127">6/29/2015</span><span class="sxs-lookup"><span data-stu-id="41158-127">6/29/2015</span></span> | <span data-ttu-id="41158-128">7/29/2015</span><span class="sxs-lookup"><span data-stu-id="41158-128">7/29/2015</span></span> | <span data-ttu-id="41158-129">10040</span><span class="sxs-lookup"><span data-stu-id="41158-129">10040</span></span>   | <span data-ttu-id="41158-130">1.000,00</span><span class="sxs-lookup"><span data-stu-id="41158-130">1,000.00</span></span>                       | <span data-ttu-id="41158-131">USD</span><span class="sxs-lookup"><span data-stu-id="41158-131">USD</span></span>      | <span data-ttu-id="41158-132">940,00</span><span class="sxs-lookup"><span data-stu-id="41158-132">940.00</span></span>           |

<span data-ttu-id="41158-133">Rabattinformationen werden am unteren Rand der Seite **Buchungen ausgleichen** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="41158-133">Discount information appears at the bottom of the **Settle transactions** page.</span></span>

|                              |           |
|------------------------------|-----------|
| <span data-ttu-id="41158-134">Skontodatum</span><span class="sxs-lookup"><span data-stu-id="41158-134">Cash discount date</span></span>           | <span data-ttu-id="41158-135">7/12/2015</span><span class="sxs-lookup"><span data-stu-id="41158-135">7/12/2015</span></span> |
| <span data-ttu-id="41158-136">Skontobetrag</span><span class="sxs-lookup"><span data-stu-id="41158-136">Cash discount amount</span></span>         | <span data-ttu-id="41158-137">60,00</span><span class="sxs-lookup"><span data-stu-id="41158-137">60.00</span></span>     |
| <span data-ttu-id="41158-138">Skonto verwenden</span><span class="sxs-lookup"><span data-stu-id="41158-138">Use cash discount</span></span>            | <span data-ttu-id="41158-139">Normal</span><span class="sxs-lookup"><span data-stu-id="41158-139">Normal</span></span>    |
| <span data-ttu-id="41158-140">Verwendetes Skonto</span><span class="sxs-lookup"><span data-stu-id="41158-140">Cash discount taken</span></span>          | <span data-ttu-id="41158-141">0,00</span><span class="sxs-lookup"><span data-stu-id="41158-141">0.00</span></span>      |
| <span data-ttu-id="41158-142">Zu verwendender Skontobetrag</span><span class="sxs-lookup"><span data-stu-id="41158-142">Cash discount amount to take</span></span> | <span data-ttu-id="41158-143">60,00</span><span class="sxs-lookup"><span data-stu-id="41158-143">60.00</span></span>     |

<span data-ttu-id="41158-144">April bucht die Zahlungserfassung.</span><span class="sxs-lookup"><span data-stu-id="41158-144">April posts the payment journal.</span></span> <span data-ttu-id="41158-145">Die Rechnung wird vollständig mit einer Zahlung von 940,00 und einem Rabatt von 60,00 ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="41158-145">The invoice is fully settled by using a payment of 940.00 and a discount of 60.00.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]