---
title: Mehrwertsteuerzahlungen und Rundungsregeln
description: In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt.
author: ShylaThompson
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: pacheren
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 97f1a30c541a302755826bb8f77205bc060ec159
ms.sourcegitcommit: 7d0cfb359a4abc7392ddb3f0b3e9539c40b7204d
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/14/2021
ms.locfileid: "5897185"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="eb509-103">Mehrwertsteuerzahlungen und Rundungsregeln</span><span class="sxs-lookup"><span data-stu-id="eb509-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eb509-104">In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt.</span><span class="sxs-lookup"><span data-stu-id="eb509-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="eb509-105">In regelmäßigen Abständen muss Mehrwertsteuer gemeldet werden und an die Steuerbehörde abgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="eb509-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="eb509-106">Dazu öffnen werden, indem die Informationen zur Bank und Beitragsmehrwertsteuerprozess in der Mehrwertsteuerseite ausführt.</span><span class="sxs-lookup"><span data-stu-id="eb509-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="eb509-107">Die Mehrwertsteuer für einen Zeitraum wird mit den Mehrwertsteuerkonten ausgeglichen und der Mehrwertsteuersaldo wird zum Konto "Mehrwertsteuerabrechnung" gebucht.</span><span class="sxs-lookup"><span data-stu-id="eb509-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="eb509-108">Der Mehrwertsteuersaldo, der im Konto "Mehrwertsteuerabrechnung" gebucht wird, kann je nach Anforderung der Steuerbehörden gerundet werden, indem eine Rundungsregel für die Mehrwertsteuerseite eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="eb509-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="eb509-109">Die Rundungsdifferenz wird zum Konto "Rundung Mehrwertsteuer" gebucht, das im Feld "Konten für automatische Buchungen" im "Hauptbuch" ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="eb509-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="eb509-110">Das Beispiel unten veranschaulicht, wie der Rundenregel bei "Mehrwertsteuerbehörde" funktioniert.</span><span class="sxs-lookup"><span data-stu-id="eb509-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="eb509-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="eb509-111">Examples</span></span>

<span data-ttu-id="eb509-112">Die Gesamtumsatzsteuer für eine Periode zeigt ein Guthaben von -98.765,43 an.</span><span class="sxs-lookup"><span data-stu-id="eb509-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="eb509-113">Die juristische Person hat mehr Mehrwertsteuer eingenommen, als sie bezahlt hat.</span><span class="sxs-lookup"><span data-stu-id="eb509-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="eb509-114">Daher schuldet die juristische Person der Steuerbehörde Geld.</span><span class="sxs-lookup"><span data-stu-id="eb509-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="eb509-115">Die juristische Person möchte eine Rundungsmethode verwenden, mit der der Saldo auf die nächsten 1,00 gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="eb509-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="eb509-116">Der Benutzer, der für die Mehrwertsteuerbuchhaltung zuständig ist, führt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="eb509-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1. <span data-ttu-id="eb509-117">Klicken Sie auf **Steuer** > **Indirekte Steuern** > **Mehrwertsteuer** > **Mehrwertsteuerbehörden**.</span><span class="sxs-lookup"><span data-stu-id="eb509-117">Click **Tax** > **Indirect taxes** > **Sales tax** > **Sales tax authorities**.</span></span>
2. <span data-ttu-id="eb509-118">Wählen Sie im Inforegister **Allgemein** im Feld **Rundungsart** die Option **Normal** aus.</span><span class="sxs-lookup"><span data-stu-id="eb509-118">On the **General** FastTab, in the **Rounding form** field, select **Normal**.</span></span>
3. <span data-ttu-id="eb509-119">Geben Sie im Feld **Rundung** die Zahl 1,00 ein.</span><span class="sxs-lookup"><span data-stu-id="eb509-119">In the **Round-off** field, enter 1.00.</span></span>
4. <span data-ttu-id="eb509-120">Wenn die Mehrwertsteuer an das Finanzamt abgeführt werden soll, wechseln Sie zu **Steuer** > **Meldungen** > **Mehrwertsteuer** > **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="eb509-120">When it is time to pay the sales taxes to the tax authority, go to **Tax** > **Declarations** > **Sales tax** > **Settle and post sale tax**.</span></span> <span data-ttu-id="eb509-121">Im Mehrwertsteuer-Abrechnungskonto können Sie sehen, dass der Steuerverbindlichkeitsbetrag von **98.765,43** auf **98.765** abgerundet wird.</span><span class="sxs-lookup"><span data-stu-id="eb509-121">On the sales tax settlement account, you can see that the tax liability amount of **98,765.43** is rounded to **98,765**.</span></span>

<span data-ttu-id="eb509-122">Die folgende Tabelle zeigt, wie ein Betrag von 98.765,43 gerundet wird. Dabei wird jede Rundungsmethode angewendet, die im Feld **Rundungsart** auf der Seite **Steuerbehörden** verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="eb509-122">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the **Rounding form** field in the **Sales tax authorities** page.</span></span>

> [!NOTE]                                                                                  
> <span data-ttu-id="eb509-123">Wenn der Rundungswert auf 0,00 eingestellt ist, gilt Folgendes:</span><span class="sxs-lookup"><span data-stu-id="eb509-123">If the round-off value is set as 0.00, then:</span></span>
>
> - <span data-ttu-id="eb509-124">Bei normaler Rundung ist das Rundungsverhalten das Gleiche wie für **Rundung = 0,01**.</span><span class="sxs-lookup"><span data-stu-id="eb509-124">For normal rounding, the rounding behavior is the same as for **Round-off = 0.01**.</span></span>
> - <span data-ttu-id="eb509-125">Für **Option der Rundungsart**, **Abrunden**, **Aufrunden** und **Eigener Vorteil** ist das Verhalten mit dem für **Rundung = 1,00** identisch.</span><span class="sxs-lookup"><span data-stu-id="eb509-125">For the **Rounding form options**, **Downward**, **Rounding-up**, and **Own advantage**, the behavior is the same as for **Round-off = 1.00**.</span></span>

| <span data-ttu-id="eb509-126">Option der Rundungsart</span><span class="sxs-lookup"><span data-stu-id="eb509-126">Rounding form option</span></span>                | <span data-ttu-id="eb509-127">Rundungswert = 0,01</span><span class="sxs-lookup"><span data-stu-id="eb509-127">Round-off value = 0.01</span></span> | <span data-ttu-id="eb509-128">Rundungswert = 0,10</span><span class="sxs-lookup"><span data-stu-id="eb509-128">Round-off value = 0.10</span></span> | <span data-ttu-id="eb509-129">Rundungswert = 1,00</span><span class="sxs-lookup"><span data-stu-id="eb509-129">Round-off value = 1.00</span></span> | <span data-ttu-id="eb509-130">Rundungswert = 100,00</span><span class="sxs-lookup"><span data-stu-id="eb509-130">Round-off value = 100.00</span></span> | <span data-ttu-id="eb509-131">Rundungswert = 0,00</span><span class="sxs-lookup"><span data-stu-id="eb509-131">Round-off value = 0.00</span></span>   |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|--------------------------|
| <span data-ttu-id="eb509-132">Normal</span><span class="sxs-lookup"><span data-stu-id="eb509-132">Normal</span></span>                              | <span data-ttu-id="eb509-133">98,765.43</span><span class="sxs-lookup"><span data-stu-id="eb509-133">98,765.43</span></span>              | <span data-ttu-id="eb509-134">98,765.40</span><span class="sxs-lookup"><span data-stu-id="eb509-134">98,765.40</span></span>              | <span data-ttu-id="eb509-135">98,765.00</span><span class="sxs-lookup"><span data-stu-id="eb509-135">98,765.00</span></span>              | <span data-ttu-id="eb509-136">98,800.00</span><span class="sxs-lookup"><span data-stu-id="eb509-136">98,800.00</span></span>                | <span data-ttu-id="eb509-137">98,765.43</span><span class="sxs-lookup"><span data-stu-id="eb509-137">98,765.43</span></span>                |
| <span data-ttu-id="eb509-138">Abwärts</span><span class="sxs-lookup"><span data-stu-id="eb509-138">Downward</span></span>                            | <span data-ttu-id="eb509-139">98,765.43</span><span class="sxs-lookup"><span data-stu-id="eb509-139">98,765.43</span></span>              | <span data-ttu-id="eb509-140">98,765.40</span><span class="sxs-lookup"><span data-stu-id="eb509-140">98,765.40</span></span>              | <span data-ttu-id="eb509-141">98,765.00</span><span class="sxs-lookup"><span data-stu-id="eb509-141">98,765.00</span></span>              | <span data-ttu-id="eb509-142">98,700.00</span><span class="sxs-lookup"><span data-stu-id="eb509-142">98,700.00</span></span>                | <span data-ttu-id="eb509-143">98,765.00</span><span class="sxs-lookup"><span data-stu-id="eb509-143">98,765.00</span></span>                |
| <span data-ttu-id="eb509-144">Aufrunden</span><span class="sxs-lookup"><span data-stu-id="eb509-144">Rounding-up</span></span>                         | <span data-ttu-id="eb509-145">98,765.43</span><span class="sxs-lookup"><span data-stu-id="eb509-145">98,765.43</span></span>              | <span data-ttu-id="eb509-146">98,765.50</span><span class="sxs-lookup"><span data-stu-id="eb509-146">98,765.50</span></span>              | <span data-ttu-id="eb509-147">98,766.00</span><span class="sxs-lookup"><span data-stu-id="eb509-147">98,766.00</span></span>              | <span data-ttu-id="eb509-148">98,800.00</span><span class="sxs-lookup"><span data-stu-id="eb509-148">98,800.00</span></span>                | <span data-ttu-id="eb509-149">98,766.00</span><span class="sxs-lookup"><span data-stu-id="eb509-149">98,766.00</span></span>                |
| <span data-ttu-id="eb509-150">Eigener Vorteil, für ein Guthaben</span><span class="sxs-lookup"><span data-stu-id="eb509-150">Own advantage, for a credit balance</span></span> | <span data-ttu-id="eb509-151">98,765.43</span><span class="sxs-lookup"><span data-stu-id="eb509-151">98,765.43</span></span>              | <span data-ttu-id="eb509-152">98,765.40</span><span class="sxs-lookup"><span data-stu-id="eb509-152">98,765.40</span></span>              | <span data-ttu-id="eb509-153">98,765.00</span><span class="sxs-lookup"><span data-stu-id="eb509-153">98,765.00</span></span>              | <span data-ttu-id="eb509-154">98,700.00</span><span class="sxs-lookup"><span data-stu-id="eb509-154">98,700.00</span></span>                | <span data-ttu-id="eb509-155">98,765.00</span><span class="sxs-lookup"><span data-stu-id="eb509-155">98,765.00</span></span>                |
| <span data-ttu-id="eb509-156">Eigener Vorteil, für ein Debitorensaldo</span><span class="sxs-lookup"><span data-stu-id="eb509-156">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="eb509-157">98,765.43</span><span class="sxs-lookup"><span data-stu-id="eb509-157">98,765.43</span></span>              | <span data-ttu-id="eb509-158">98,765.50</span><span class="sxs-lookup"><span data-stu-id="eb509-158">98,765.50</span></span>              | <span data-ttu-id="eb509-159">98,766.00</span><span class="sxs-lookup"><span data-stu-id="eb509-159">98,766.00</span></span>              | <span data-ttu-id="eb509-160">98,800.00</span><span class="sxs-lookup"><span data-stu-id="eb509-160">98,800.00</span></span>                | <span data-ttu-id="eb509-161">98,766.00</span><span class="sxs-lookup"><span data-stu-id="eb509-161">98,766.00</span></span>                |

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="eb509-162">Normale Rundung und Rungungsgenauigkeit ist 0,01</span><span class="sxs-lookup"><span data-stu-id="eb509-162">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="eb509-163">Rundung</span><span class="sxs-lookup"><span data-stu-id="eb509-163">Rounding</span></span>
    </td>
    <td><span data-ttu-id="eb509-164">Berechnungsprozess</span><span class="sxs-lookup"><span data-stu-id="eb509-164">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="eb509-165">Rundung(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="eb509-165">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="eb509-166">Rundung(1,015 / 0,01, 0) = Rundung(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="eb509-166">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="eb509-167">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="eb509-167">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="eb509-168">Rundung(1,014 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="eb509-168">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="eb509-169">Rundung(1,014 / 0,01, 0) = Rundung(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="eb509-169">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="eb509-170">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="eb509-170">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="eb509-171">Rundung(1,011 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="eb509-171">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="eb509-172">Rundung(1,011 / 0,02, 0) = Rundung(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="eb509-172">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="eb509-173">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="eb509-173">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="eb509-174">Rundung(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="eb509-174">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="eb509-175">Rundung(1,009 / 0,02, 0) = Rundung(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="eb509-175">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="eb509-176">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="eb509-176">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="eb509-177">Wenn Sie "Eigener Vorteil" auswählen, erfolgt die Rundung immer zum Vorteil der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="eb509-177">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="eb509-178">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="eb509-178">For more information, see the following topics:</span></span>
- [<span data-ttu-id="eb509-179">Mehrwertsteuerübersicht</span><span class="sxs-lookup"><span data-stu-id="eb509-179">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="eb509-180">Eine Mehrwertsteuerzahlung erstellen</span><span class="sxs-lookup"><span data-stu-id="eb509-180">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="eb509-181">Mehrwertsteuerbuchungen in Dokumenten erstellen</span><span class="sxs-lookup"><span data-stu-id="eb509-181">Create sales tax transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="eb509-182">Vorgenommene Mehrwertsteuerbuchungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="eb509-182">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- <span data-ttu-id="eb509-183">[Rundungsfunktion](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))</span><span class="sxs-lookup"><span data-stu-id="eb509-183">[round Function](/previous-versions/dynamics/ax-2012/reference/aa850656(v=ax.60))</span></span>




[!INCLUDE[footer-include](../../includes/footer-banner.md)]
