---
title: Skonti
description: Skonti werden für Kreditoren und Debitoren eingerichtet und freigegeben.  Das verfügbare Skonto kann auf der Debitorenrechnung oder der Kreditorenrechnung definiert werden und wird übernommen, wenn die Rechnung innerhalb des Skontodatums bezahlt wird.
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 139fb4fdb7d4f8034bff5e9668dc794f29fb327e
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4443717"
---
# <a name="cash-discounts"></a><span data-ttu-id="96aa8-104">Skonti</span><span class="sxs-lookup"><span data-stu-id="96aa8-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="96aa8-105">Skonti werden für Kreditoren und Debitoren eingerichtet und freigegeben.</span><span class="sxs-lookup"><span data-stu-id="96aa8-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="96aa8-106">Das verfügbare Skonto kann auf der Debitorenrechnung oder der Kreditorenrechnung definiert werden und wird übernommen, wenn die Rechnung innerhalb des Skontodatums bezahlt wird.</span><span class="sxs-lookup"><span data-stu-id="96aa8-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="96aa8-107">Skonti</span><span class="sxs-lookup"><span data-stu-id="96aa8-107">Cash discounts</span></span>

<span data-ttu-id="96aa8-108">Skonti für Debitoren oder Kreditoren können auf der Skontoseite erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="96aa8-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="96aa8-109">Mithilfe des Felds "Nächster Skontocode" können Sie zudem eine Reihe von aufeinander folgenden Skonti definieren, die aufeinander folgen.</span><span class="sxs-lookup"><span data-stu-id="96aa8-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="96aa8-110">Weitere Informationen finden Sie weiter unten in diesem Thema unter "Beispiel: Reihe von aufeinander folgenden Skonti".</span><span class="sxs-lookup"><span data-stu-id="96aa8-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="96aa8-111">Wenn die Rechnung, die Habenbuchung (entweder Zahlung oder Gutschrift) oder beide nicht in einer Buchungswährung der juristischen Person eingegeben werden, wird das Skonto basierend auf dem Wechselkurs für Skonti für das Datum der Zahlung oder der Gutschrift berechnet.</span><span class="sxs-lookup"><span data-stu-id="96aa8-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="96aa8-112">Wenn die Rechnung und das Habendokument in verschiedenen juristischen Personen erfasst werden und die Buchhaltungswährungen der juristischen Personen unterschiedlich sind, wird der Wechselkurs der juristischen Person der Rechnung verwendet, der am Datum des Habendokuments gültig ist.</span><span class="sxs-lookup"><span data-stu-id="96aa8-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="96aa8-113">Weitere Informationen finden Sie weiter unten in diesem Thema unter "Beispiel: Wechselkurse für Skonti".</span><span class="sxs-lookup"><span data-stu-id="96aa8-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="96aa8-114">Standardreihenfolge des Skonto-Hauptkontos</span><span class="sxs-lookup"><span data-stu-id="96aa8-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="96aa8-115">Wird eine Rechnung so frühzeitig beglichen, dass ein Skonto gewährt wird, so wird das Skonto automatisch auf ein Hauptkonto gebucht. Hierbei gilt folgende Standardpriorität:</span><span class="sxs-lookup"><span data-stu-id="96aa8-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="96aa8-116">Das Hauptkonto, das im alternativen Feld "Alternatives Skontokonto" auf der Seite "Offene Buchungen ausgleichen" oder auf der Seite "Offene Buchungen ausgleichen" des Kreditors angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="96aa8-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="96aa8-117">Das Hauptkonto, das im Feld "Debitorenskonto" oder im Feld "Kreditorenskonto" der Sachkontobuchungsgruppe angegeben ist, die dem Mehrwertsteuercode der Rechnung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="96aa8-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="96aa8-118">Richten Sie Sachkontobuchungsgruppen auf der Sachkontobuchungsgruppenseite ein und weisen Sie sie zu Mehrwertsteuercodes in der Mehrwertsteuercodeseite zu.</span><span class="sxs-lookup"><span data-stu-id="96aa8-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="96aa8-119">Das Hauptbuchungskonto, das auf der Seite "Skonti" entweder im Feld "Hauptkonto für Debitorenrabatte" oder im Feld "Hauptkonto für Kreditorenrabatte" für den Skontocode auf der ausgeglichenen Rechnung angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="96aa8-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="96aa8-120">Das Hauptkonto für Skonti, wie in auf der Seite "Konten für automatische Buchungen" angegeben.</span><span class="sxs-lookup"><span data-stu-id="96aa8-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="96aa8-121"> Beispiel: Reihe von aufeinander folgenden Skonti</span><span class="sxs-lookup"><span data-stu-id="96aa8-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="96aa8-122">Richten Sie wie nachstehend gezeigt drei Skontocodes ein:</span><span class="sxs-lookup"><span data-stu-id="96aa8-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="96aa8-123">Code 5D10% – Skonto von 10 %, wenn der Betrag innerhalb von 5 Tagen beglichen wird.</span><span class="sxs-lookup"><span data-stu-id="96aa8-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="96aa8-124">Code 10D5% – Skonto von 5 %, wenn der Betrag innerhalb von 10 Tagen beglichen wird.</span><span class="sxs-lookup"><span data-stu-id="96aa8-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="96aa8-125">Code 14D2% – Skonto von 2 %, wenn der Betrag innerhalb von 14 Tagen beglichen wird.</span><span class="sxs-lookup"><span data-stu-id="96aa8-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="96aa8-126">Wählen Sie im Feld "Nächster Skontocode":</span><span class="sxs-lookup"><span data-stu-id="96aa8-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="96aa8-127">Wählen Sie 10D5% für den Code 5D10%.</span><span class="sxs-lookup"><span data-stu-id="96aa8-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="96aa8-128">Wählen Sie 14D2% für den Code 10D5%.</span><span class="sxs-lookup"><span data-stu-id="96aa8-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="96aa8-129">Lassen Sie für den Code "14D2%" das Feld "Nächster Skontocode" leer.</span><span class="sxs-lookup"><span data-stu-id="96aa8-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="96aa8-130">Diese drei Skonti folgen aufeinander da das Zahlungsdatum nach dem vorherigen Skontodatum der Rechnung liegt.</span><span class="sxs-lookup"><span data-stu-id="96aa8-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="96aa8-131">Nur ein Skonto wird gewährt, wenn die Rechnung bezahlt wird. Dies basiert darauf, welches Skontodatum in der Folge von Skontos gilt.</span><span class="sxs-lookup"><span data-stu-id="96aa8-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="96aa8-132"> Beispiel: Wechselkurse für Skonti</span><span class="sxs-lookup"><span data-stu-id="96aa8-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="96aa8-133">Die Buchhaltungswährung der juristischen Person ist EUR, und für US-Dollar sind folgende Wechselkurse angegeben:</span><span class="sxs-lookup"><span data-stu-id="96aa8-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="96aa8-134">1. Februar = 110</span><span class="sxs-lookup"><span data-stu-id="96aa8-134">February 1 = 110</span></span>
-   <span data-ttu-id="96aa8-135">1. März = 80</span><span class="sxs-lookup"><span data-stu-id="96aa8-135">March 1 = 80</span></span>

<span data-ttu-id="96aa8-136">Eine Rechnung in Höhe von 1.000 US-Dollar mit den Skontobedingungen von 20D2% wird am 15. Februar gebucht.</span><span class="sxs-lookup"><span data-stu-id="96aa8-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="96aa8-137">Der Rechnungsbetrag in der Buchhaltungswährung beträgt 1.100 EUR.</span><span class="sxs-lookup"><span data-stu-id="96aa8-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="96aa8-138">Eine Zahlung in Höhe von 980 US-Dollar wird mit der Rechnung vom 1. März ausgeglichen.</span><span class="sxs-lookup"><span data-stu-id="96aa8-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="96aa8-139">Der Skontobetrag ist 20 US-Dollar.</span><span class="sxs-lookup"><span data-stu-id="96aa8-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="96aa8-140">Der Zahlungsbetrag in der Buchhaltungswährung ist 784 EUR.</span><span class="sxs-lookup"><span data-stu-id="96aa8-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="96aa8-141">Der Buchhaltungswährungsbetrag des Skontos wird mit dem Wechselkurs am 1. März berechnet: 20 \* 80 / 100 = 16 EUR.</span><span class="sxs-lookup"><span data-stu-id="96aa8-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="96aa8-142">Wenn die Option "Skonti für Teilzahlungen berechnen" auf der Debitorenparameter- oder Kreditorenparameterseite aktiviert ist, wird der Wechselkurs, der am Tag der jeweiligen Teilzahlung gültig ist, verwendet.</span><span class="sxs-lookup"><span data-stu-id="96aa8-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 

