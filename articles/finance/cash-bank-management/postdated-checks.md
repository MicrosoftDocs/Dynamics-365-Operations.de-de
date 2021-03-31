---
title: Vordatierte Schecks
description: Dieser Artikel enthält Informationen über die Unterstützung bei vordatierten Prüfungen in Microsoft Dynamics 365 Finance. Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können. Daher kann der Scheck nicht bis zum angegebene Datum eingewechselt werden.
author: ShylaThompson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: roschlom
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7562999a09e0036a7ea765c0cb0954412bbbda69
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5228862"
---
# <a name="postdated-checks"></a><span data-ttu-id="b40f9-105">Vordatierte Schecks</span><span class="sxs-lookup"><span data-stu-id="b40f9-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b40f9-106">Dieser Artikel enthält Informationen über die Unterstützung bei vordatierten Prüfungen.</span><span class="sxs-lookup"><span data-stu-id="b40f9-106">This article provides information about support for postdated checks.</span></span> <span data-ttu-id="b40f9-107">Vordatierte Schecks sind Schecks, die ausgestellt werden, um Zahlungen zu einem späteren Datum leisten oder erhalten zu können.</span><span class="sxs-lookup"><span data-stu-id="b40f9-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="b40f9-108">Daher kann der Scheck nicht bis zum angegebene Datum eingewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="b40f9-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="b40f9-109">Dynamics 365 Finance unterstützt den vollständigen Verwaltungszyklus für vordatierte Prüfungen in Debitoren und Kreditoren wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b40f9-109">Dynamics 365 Finance supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b40f9-110">Szenario</span><span class="sxs-lookup"><span data-stu-id="b40f9-110">Scenario</span></span></th>
<th><span data-ttu-id="b40f9-111">Details</span><span class="sxs-lookup"><span data-stu-id="b40f9-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b40f9-112">Einrichten von vordatierten Schecks</span><span class="sxs-lookup"><span data-stu-id="b40f9-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="b40f9-113">Sie müssen eine neue Zahlungsmethode einrichten und definieren die Zahlungsroutine für das Vorbereiten für ausgegebene Schecks, Erhaltene Schecks und Quellensteuer.</span><span class="sxs-lookup"><span data-stu-id="b40f9-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b40f9-114">Erfassen und Buchen eines vordatierten Schecks für einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="b40f9-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="b40f9-115">Erfassung eines vordatierten Schecks, bevor der Scheck an einen Kreditor ausgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b40f9-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="b40f9-116">Wenn die Zahlung gebucht wird, werden die die Verbindlichkeiten dem Kreditor gegenüber erkannt, doch der Betrag wurde dem Bankkonto noch nicht gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="b40f9-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="b40f9-117">Stattdessen wird ein Verrechnungskonto für diesen Zweck verwendet.</span><span class="sxs-lookup"><span data-stu-id="b40f9-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b40f9-118">Erfassen und Buchen eines vordatierten Schecks von einem Debitor</span><span class="sxs-lookup"><span data-stu-id="b40f9-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="b40f9-119">Sie können die Details eines vordatierten Schecks erfassen, den Sie von einem Debitor erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="b40f9-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="b40f9-120">Wenn die Zahlung gebucht wird, werden die die Verbindlichkeiten dem Kreditor gegenüber erkannt, doch der Betrag wurde dem Bankkonto noch nicht gutgeschrieben.</span><span class="sxs-lookup"><span data-stu-id="b40f9-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="b40f9-121">Stattdessen wird ein Verrechnungskonto für diesen Zweck verwendet.</span><span class="sxs-lookup"><span data-stu-id="b40f9-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b40f9-122">Erfassen und Buchen eines vordatierten Ersatzschecks für einen Kunden oder einen Händler.</span><span class="sxs-lookup"><span data-stu-id="b40f9-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="b40f9-123">Wenn Ihr Originalscheck an einen Händler oder von einem Kunden verloren ging oder beschädigt wird, können Sie für den Kreditor einen vordatierten Ersatzscheck ausstellen.</span><span class="sxs-lookup"><span data-stu-id="b40f9-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="b40f9-124">Geben Sie beim Erfassen der Scheckdetails einen Verweis auf den Originalscheck an, und weisen Sie darauf hin, dass der neue Scheck als Ersatz für das Original gilt.</span><span class="sxs-lookup"><span data-stu-id="b40f9-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="b40f9-125">Sie können den Ersatzscheck auch buchen.</span><span class="sxs-lookup"><span data-stu-id="b40f9-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b40f9-126">Übertragen eines vordatierten Debitorenschecks an einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="b40f9-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="b40f9-127">Wenn Sie von einem Kunden einen vordatierten Scheck erhalten, können Sie diesen Scheck als Zahlung an einen Kreditor übermitteln.</span><span class="sxs-lookup"><span data-stu-id="b40f9-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b40f9-128">Ausgleichen eines vordatierten Schecks für einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="b40f9-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="b40f9-129">Verwenden Sie das Formular , um einen rückdatierten Scheck auszugleichen, der für einen Debitor oder Kreditor auf ein Transferkonto gebucht wurde.</span><span class="sxs-lookup"><span data-stu-id="b40f9-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="b40f9-130">Wenn der Scheck ausgeglichen wird, ist die Bank schließlich Soll oder Haben für das Verrechnungskonto, das zuvor verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b40f9-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b40f9-131">Stornieren eines vordatierten Schecks für einen Kreditor</span><span class="sxs-lookup"><span data-stu-id="b40f9-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="b40f9-132">Sie können einen gebuchten vordatierten Scheck in diesen Fällen stornieren: - Die Bank verweigert die Annahme des Schecks.</span><span class="sxs-lookup"><span data-stu-id="b40f9-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="b40f9-133">- Der Scheck wurde auf eine falsche Rechnung angewendet.</span><span class="sxs-lookup"><span data-stu-id="b40f9-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="b40f9-134">- Für den Betrag des Schecks wird eine Barzahlung geleistet.</span><span class="sxs-lookup"><span data-stu-id="b40f9-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="b40f9-135">Beenden der Zahlung eines vordatierten Schecks.</span><span class="sxs-lookup"><span data-stu-id="b40f9-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="b40f9-136">Sie können die Zahlung für einen vordatierten Scheck stoppen, der für einen Kreditor ausgestellt wurde. Gründe dafür können eine mangelnde Deckung, eine Änderung der vertraglichen Vereinbarungen mit dem Kreditor, die Lieferung fehlerhafter Waren durch den Kreditor oder die Rückgabe von Waren an den Kreditor sein.</span><span class="sxs-lookup"><span data-stu-id="b40f9-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="b40f9-137">Sie können Zahlungen nur für Schecks stoppen, die noch nicht verrechnet wurden.</span><span class="sxs-lookup"><span data-stu-id="b40f9-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="b40f9-138">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b40f9-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="b40f9-139">Vordatierte Schecks einrichten</span><span class="sxs-lookup"><span data-stu-id="b40f9-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="b40f9-140">Einen vordatierten Scheck für einen Debitor erfassen und buchen</span><span class="sxs-lookup"><span data-stu-id="b40f9-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="b40f9-141">Einen vordatierten Scheck von einem Debitor ausgleichen</span><span class="sxs-lookup"><span data-stu-id="b40f9-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="b40f9-142">Einen vordatierten Scheck für einen Kreditor erfassen und buchen</span><span class="sxs-lookup"><span data-stu-id="b40f9-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="b40f9-143">Einen vordatierten Scheck für einen Kreditor ausgleichen</span><span class="sxs-lookup"><span data-stu-id="b40f9-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]