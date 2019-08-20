---
title: Mehrwertsteuerzahlungen und Rundungsregeln
description: In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt.
author: ShylaThompson
manager: AnnBe
ms.date: 05/30/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 6134
ms.assetid: 7dcd3cf5-ebdf-4a9f-806c-1296c7da0331
ms.search.region: Global
ms.author: yijialuan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 168c2fb9edfc994617ef6764a5b9f5949d599882
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834997"
---
# <a name="sales-tax-payments-and-rounding-rules"></a><span data-ttu-id="b1e68-103">Mehrwertsteuerzahlungen und Rundungsregeln</span><span class="sxs-lookup"><span data-stu-id="b1e68-103">Sales tax payments and rounding rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1e68-104">In diesem Artikel wird beschrieben, wie sich die Rundungsregeleinstellung auf die Mehrwertsteuer-Behörden und auf die Rundung des Mehrwertsteuersaldos während der Abrechnung und Buchung der Mehrwertsteuer auswirkt.</span><span class="sxs-lookup"><span data-stu-id="b1e68-104">This article explains how the rounding rule setup on the Sales tax authorities works and rounding the sales tax balance during the Settle and post sales tax job.</span></span>

<span data-ttu-id="b1e68-105">In regelmäßigen Abständen muss Mehrwertsteuer gemeldet werden und an die Steuerbehörde abgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b1e68-105">Periodically, sales tax needs to be reported and paid to tax authorities.</span></span> <span data-ttu-id="b1e68-106">Dazu öffnen werden, indem die Informationen zur Bank und Beitragsmehrwertsteuerprozess in der Mehrwertsteuerseite ausführt.</span><span class="sxs-lookup"><span data-stu-id="b1e68-106">This can be done by running the settle and post sales tax process in the Sales tax page.</span></span> <span data-ttu-id="b1e68-107">Die Mehrwertsteuer für einen Zeitraum wird mit den Mehrwertsteuerkonten ausgeglichen und der Mehrwertsteuersaldo wird zum Konto "Mehrwertsteuerabrechnung" gebucht.</span><span class="sxs-lookup"><span data-stu-id="b1e68-107">Sales tax for a period will be settled against the sales tax accounts and the sales tax balance will be posted to the Sales tax settlement account.</span></span> <span data-ttu-id="b1e68-108">Der Mehrwertsteuersaldo, der im Konto "Mehrwertsteuerabrechnung" gebucht wird, kann je nach Anforderung der Steuerbehörden gerundet werden, indem eine Rundungsregel für die Mehrwertsteuerseite eingerichtet wird.</span><span class="sxs-lookup"><span data-stu-id="b1e68-108">The sales tax balance, which is posted on the Sales tax settlement account, can be rounded as required by tax authorities by setting up a rounding rule on the Sales tax page.</span></span> 

<span data-ttu-id="b1e68-109">Die Rundungsdifferenz wird zum Konto "Rundung Mehrwertsteuer" gebucht, das im Feld "Konten für automatische Buchungen" im "Hauptbuch" ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b1e68-109">The rounding difference is posted to the Sales tax rounding account that is selected in the Accounts for automatic transactions field in the General ledger.</span></span>

<span data-ttu-id="b1e68-110">Das Beispiel unten veranschaulicht, wie der Rundenregel bei "Mehrwertsteuerbehörde" funktioniert.</span><span class="sxs-lookup"><span data-stu-id="b1e68-110">The below example illustrates how the rounding rule on Sales tax authority works.</span></span>

## <a name="examples"></a><span data-ttu-id="b1e68-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b1e68-111">Examples</span></span>

<span data-ttu-id="b1e68-112">Die Gesamtumsatzsteuer für eine Periode zeigt ein Guthaben von -98.765,43 an.</span><span class="sxs-lookup"><span data-stu-id="b1e68-112">The total sales tax for a period shows a credit balance of -98,765.43.</span></span> <span data-ttu-id="b1e68-113">Die juristische Person hat mehr Mehrwertsteuer eingenommen, als sie bezahlt hat.</span><span class="sxs-lookup"><span data-stu-id="b1e68-113">The legal entity collected more sales taxes than it paid.</span></span> <span data-ttu-id="b1e68-114">Daher schuldet die juristische Person der Steuerbehörde Geld.</span><span class="sxs-lookup"><span data-stu-id="b1e68-114">Therefore, the legal entity owes money to the tax authority.</span></span> 

<span data-ttu-id="b1e68-115">Die juristische Person möchte eine Rundungsmethode verwenden, mit der der Saldo auf die nächsten 1,00 gerundet wird.</span><span class="sxs-lookup"><span data-stu-id="b1e68-115">The legal entity wants to use a rounding method that rounds the balance to the nearest 1.00.</span></span> <span data-ttu-id="b1e68-116">Der Benutzer, der für die Mehrwertsteuerbuchhaltung zuständig ist, führt die folgenden Schritte aus.</span><span class="sxs-lookup"><span data-stu-id="b1e68-116">The user who is responsible for sales tax accounting performs the following steps.</span></span>

1.  <span data-ttu-id="b1e68-117">Klicken Sie auf "Steuer" &gt; "Indirekte Steuern" &gt; "Mehrwertsteuer" &gt; "Mehrwertsteuerbehörden".</span><span class="sxs-lookup"><span data-stu-id="b1e68-117">Click Tax &gt; Indirect taxes &gt; Sales tax &gt; Sales tax authorities</span></span>
2.  <span data-ttu-id="b1e68-118">Wählen Sie im Inforegister "Allgemein" im Feld "Rundungsart" die Option "Normal" aus.</span><span class="sxs-lookup"><span data-stu-id="b1e68-118">On the General FastTab, select Normal in the Rounding form field.</span></span>
3.  <span data-ttu-id="b1e68-119">Geben Sie im Feld "Rundung" die Zahl 1,00 ein.</span><span class="sxs-lookup"><span data-stu-id="b1e68-119">In the Round-off field, enter 1.00.</span></span>
4.  <span data-ttu-id="b1e68-120">Wenn die Mehrwertsteuer an das Finanzamt abgeführt werden soll, öffnen Sie die Seite "Mehrwertsteuer abrechnen und buchen".</span><span class="sxs-lookup"><span data-stu-id="b1e68-120">When it is time to pay the sales taxes to the tax authority, open the Settle and post sales tax page.</span></span> <span data-ttu-id="b1e68-121">(Klicken Sie auf "Steuer" &gt; "Erklärungen" &gt; "Mehrwertsteuer" &gt; "Mehrwertsteuer abrechnen und buchen".)</span><span class="sxs-lookup"><span data-stu-id="b1e68-121">(Click Tax &gt; Declarations &gt; Sales tax &gt; Settle and post sales tax.)</span></span>
5.  <span data-ttu-id="b1e68-122">Im Mehrwertsteuer-Abrechnungskonto wird der Steuerverbindlichkeitsbetrag von 98.765,43 auf 98.765 abgerundet.</span><span class="sxs-lookup"><span data-stu-id="b1e68-122">On the sales tax settlement account, the tax liability amount of 98,765.43 is rounded to 98,765.</span></span>

<span data-ttu-id="b1e68-123">Die folgende Tabelle zeigt, wie ein Betrag von 98.765,43 gerundet wird. Dabei wird jede Rundungsmethode angewendet, die im Feld "Rundungsart" auf der Seite "Steuerbehörden" verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b1e68-123">The following table shows how an amount of 98,765.43 is rounded by using each rounding method that is available in the Rounding form field in the Sales tax authorities page.</span></span>

| <span data-ttu-id="b1e68-124">Option der Rundungsart</span><span class="sxs-lookup"><span data-stu-id="b1e68-124">Rounding form option</span></span>                | <span data-ttu-id="b1e68-125">Rundungswert = 0,01</span><span class="sxs-lookup"><span data-stu-id="b1e68-125">Round-off value = 0.01</span></span> | <span data-ttu-id="b1e68-126">Rundungswert = 0,10</span><span class="sxs-lookup"><span data-stu-id="b1e68-126">Round-off value = 0.10</span></span> | <span data-ttu-id="b1e68-127">Rundungswert = 1,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-127">Round-off value = 1.00</span></span> | <span data-ttu-id="b1e68-128">Rundungswert = 100,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-128">Round-off value = 100.00</span></span> |
|-------------------------------------|------------------------|------------------------|------------------------|--------------------------|
| <span data-ttu-id="b1e68-129">Normal</span><span class="sxs-lookup"><span data-stu-id="b1e68-129">Normal</span></span>                              | <span data-ttu-id="b1e68-130">98.765,43</span><span class="sxs-lookup"><span data-stu-id="b1e68-130">98,765.43</span></span>              | <span data-ttu-id="b1e68-131">98.765,40</span><span class="sxs-lookup"><span data-stu-id="b1e68-131">98,765.40</span></span>              | <span data-ttu-id="b1e68-132">98.765,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-132">98,765.00</span></span>              | <span data-ttu-id="b1e68-133">98.800,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-133">98,800.00</span></span>                |
| <span data-ttu-id="b1e68-134">Abwärts</span><span class="sxs-lookup"><span data-stu-id="b1e68-134">Downward</span></span>                            | <span data-ttu-id="b1e68-135">98.765,43</span><span class="sxs-lookup"><span data-stu-id="b1e68-135">98,765.43</span></span>              | <span data-ttu-id="b1e68-136">98.765,40</span><span class="sxs-lookup"><span data-stu-id="b1e68-136">98,765.40</span></span>              | <span data-ttu-id="b1e68-137">98.765,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-137">98,765.00</span></span>              | <span data-ttu-id="b1e68-138">98.700,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-138">98,700.00</span></span>                |
| <span data-ttu-id="b1e68-139">Aufrunden</span><span class="sxs-lookup"><span data-stu-id="b1e68-139">Rounding-up</span></span>                         | <span data-ttu-id="b1e68-140">98.765,43</span><span class="sxs-lookup"><span data-stu-id="b1e68-140">98,765.43</span></span>              | <span data-ttu-id="b1e68-141">98.765,50</span><span class="sxs-lookup"><span data-stu-id="b1e68-141">98,765.50</span></span>              | <span data-ttu-id="b1e68-142">98.766,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-142">98,766.00</span></span>              | <span data-ttu-id="b1e68-143">98.800,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-143">98,800.00</span></span>                |
| <span data-ttu-id="b1e68-144">Eigener Vorteil, für ein Guthaben</span><span class="sxs-lookup"><span data-stu-id="b1e68-144">Own advantage, for a credit balance</span></span> | <span data-ttu-id="b1e68-145">98.765,43</span><span class="sxs-lookup"><span data-stu-id="b1e68-145">98,765.43</span></span>              | <span data-ttu-id="b1e68-146">98.765,40</span><span class="sxs-lookup"><span data-stu-id="b1e68-146">98,765.40</span></span>              | <span data-ttu-id="b1e68-147">98.765,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-147">98,765.00</span></span>              | <span data-ttu-id="b1e68-148">98.700,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-148">98,700.00</span></span>                |
| <span data-ttu-id="b1e68-149">Eigener Vorteil, für ein Debitorensaldo</span><span class="sxs-lookup"><span data-stu-id="b1e68-149">Own advantage, for a debit balance</span></span>  | <span data-ttu-id="b1e68-150">98,765.43</span><span class="sxs-lookup"><span data-stu-id="b1e68-150">98,765.43</span></span>              | <span data-ttu-id="b1e68-151">98,765.50</span><span class="sxs-lookup"><span data-stu-id="b1e68-151">98,765.50</span></span>              | <span data-ttu-id="b1e68-152">98,766.00</span><span class="sxs-lookup"><span data-stu-id="b1e68-152">98,766.00</span></span>              | <span data-ttu-id="b1e68-153">98,800.00</span><span class="sxs-lookup"><span data-stu-id="b1e68-153">98,800.00</span></span>                |


### <a name="no-rounding-at-all-since-the-round-off-is-000"></a><span data-ttu-id="b1e68-154">Kein Runden, da die Rundung 0,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-154">No rounding at all, since the round-off is 0.00</span></span>

<span data-ttu-id="b1e68-155">Rundung(1,0151, 0,00) = 1,0151 Rundung(1,0149, 0,00) = 1,0149</span><span class="sxs-lookup"><span data-stu-id="b1e68-155">round(1.0151, 0.00) = 1.0151 round(1.0149, 0.00) = 1.0149</span></span>

### <a name="normal-round-and-round-precision-is-001"></a><span data-ttu-id="b1e68-156">Normale Rundung und Rungungsgenauigkeit ist 0,01</span><span class="sxs-lookup"><span data-stu-id="b1e68-156">Normal round, and round precision is 0.01</span></span>

<table>
  <tr>
    <td><span data-ttu-id="b1e68-157">Rundung</span><span class="sxs-lookup"><span data-stu-id="b1e68-157">Rounding</span></span>
    </td>
    <td><span data-ttu-id="b1e68-158">Berechnungsprozess</span><span class="sxs-lookup"><span data-stu-id="b1e68-158">Calculation process</span></span>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="b1e68-159">Rundung(1,015, 0,01) = 1,02</span><span class="sxs-lookup"><span data-stu-id="b1e68-159">round(1.015, 0.01) = 1.02</span></span>
    </td>
    <td>
      <ol>
        <li><span data-ttu-id="b1e68-160">Rundung(1,015 / 0,01, 0) = Rundung(101,5, 0) = 102</span><span class="sxs-lookup"><span data-stu-id="b1e68-160">round(1.015 / 0.01, 0) = round(101.5, 0) = 102</span></span>
        </li>
        <li><span data-ttu-id="b1e68-161">102 \* 0.01 = 1.02</span><span class="sxs-lookup"><span data-stu-id="b1e68-161">102 \* 0.01 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="b1e68-162">Rundung(1,014 0,01) = 1,01</span><span class="sxs-lookup"><span data-stu-id="b1e68-162">round(1.014, 0.01) = 1.01</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="b1e68-163">Rundung(1,014 / 0,01, 0) = Rundung(101,4, 0) = 101</span><span class="sxs-lookup"><span data-stu-id="b1e68-163">round(1.014 / 0.01, 0) = round(101.4, 0) = 101</span></span>
        </li>
        <li><span data-ttu-id="b1e68-164">101 \* 0.01 = 1.01</span><span class="sxs-lookup"><span data-stu-id="b1e68-164">101 \* 0.01 = 1.01</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="b1e68-165">Rundung(1,011 0,02) = 1,02</span><span class="sxs-lookup"><span data-stu-id="b1e68-165">round(1.011, 0.02) = 1.02</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="b1e68-166">Rundung(1,011 / 0,02, 0) = Rundung(50,55, 0) = 51</span><span class="sxs-lookup"><span data-stu-id="b1e68-166">round(1.011 / 0.02, 0) = round(50.55, 0) = 51</span></span>
        </li>
        <li><span data-ttu-id="b1e68-167">51 \* 0.02 = 1.02</span><span class="sxs-lookup"><span data-stu-id="b1e68-167">51 \* 0.02 = 1.02</span></span>
        </li>
      </ol>
    </td>
  </tr>
    <tr>
    <td><span data-ttu-id="b1e68-168">Rundung(1,009, 0,02) = 1,00</span><span class="sxs-lookup"><span data-stu-id="b1e68-168">round(1.009, 0.02) = 1.00</span></span>
    </td>
    <td> <ol>
        <li><span data-ttu-id="b1e68-169">Rundung(1,009 / 0,02, 0) = Rundung(50,45, 0) = 50</span><span class="sxs-lookup"><span data-stu-id="b1e68-169">round(1.009 / 0.02, 0) = round(50.45, 0) = 50</span></span>
        </li>
        <li><span data-ttu-id="b1e68-170">50 \* 0.02 = 1.00</span><span class="sxs-lookup"><span data-stu-id="b1e68-170">50 \* 0.02 = 1.00</span></span>
        </li>
      </ol>
    </td>
  </tr>
</table>

> [!NOTE]                                                                                  
> <span data-ttu-id="b1e68-171">Wenn Sie "Eigener Vorteil" auswählen, erfolgt die Rundung immer zum Vorteil der juristischen Person.</span><span class="sxs-lookup"><span data-stu-id="b1e68-171">If you select Own advantage, the rounding is always to the advantage of the legal entity.</span></span> 

<span data-ttu-id="b1e68-172">Weitere Informationen finden Sie in folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b1e68-172">For more information, see the following topics:</span></span>
- [<span data-ttu-id="b1e68-173">Mehrwertsteuerüberblick</span><span class="sxs-lookup"><span data-stu-id="b1e68-173">Sales tax overview</span></span>](indirect-taxes-overview.md)
- [<span data-ttu-id="b1e68-174">Eine Mehrwertsteuerzahlung erstellen</span><span class="sxs-lookup"><span data-stu-id="b1e68-174">Create a sales tax payment</span></span>](tasks/create-sales-tax-payment.md)
- [<span data-ttu-id="b1e68-175">Mehrwertsteuerbuchungen in Dokumenten erstellen</span><span class="sxs-lookup"><span data-stu-id="b1e68-175">Create sales transactions on documents</span></span>](tasks/create-sales-tax-transactions-documents.md)
- [<span data-ttu-id="b1e68-176">Vorgenommene Mehrwertsteuerbuchungen anzeigen</span><span class="sxs-lookup"><span data-stu-id="b1e68-176">View posted sales tax transactions</span></span>](tasks/view-posted-sales-tax-transactions.md)
- [<span data-ttu-id="b1e68-177">Rundungsfunktion</span><span class="sxs-lookup"><span data-stu-id="b1e68-177">round Function</span></span>](https://msdn.microsoft.com/library/aa850656.aspx)


