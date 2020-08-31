---
title: Mehrwertsteuerberechnung für allgemeine Erfassungspositionen
description: In diesem Thema wird erläutert, wie die Mehrwertsteuer für verschiedene Kontotypen (Kreditorenkonto, Debitorenkonto, Sachkonto und Projekt) in allgemeinen Erfassungspositionen berechnet werden.
author: EricWang
manager: Ann Beebe
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 93c9f2bebd038723d50e64bdaa0e0992c003f88d
ms.sourcegitcommit: cec5de2dcfc7210a86a220e308f80ab204f12383
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665841"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="fb6a7-103">Mehrwertsteuerberechnung für allgemeine Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="fb6a7-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb6a7-104">In diesem Thema wird erläutert, wie die Mehrwertsteuer für verschiedene Kontotypen (Kreditorenkonto, Debitorenkonto, Sachkonto und Projekt) in allgemeinen Erfassungspositionen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="fb6a7-105">Der Prozess kann in drei Schritte unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="fb6a7-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="fb6a7-106">Ermitteln der Mehrwertsteuerart.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="fb6a7-107">Festlegen des Mehrwertsteuerbetrags, der in einer temporären Mehrwertsteuertabelle gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="fb6a7-108">Bestimmen des Mehrwertsteuerbetrags und des Kontos für den Beleg.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="fb6a7-109">Ermitteln der Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="fb6a7-109">Determine the sales tax direction</span></span>

<span data-ttu-id="fb6a7-110">Die Methode, mit der die Mehrwertsteuerart bestimmt wird, hängt von der Art des Kontos im Beleg ab.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="fb6a7-111">Die Mehrwertsteuerart wird durch die Kombination aus Kontenart und Mehrwertsteuercodes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="fb6a7-112">In den folgenden Abschnitten sind die Möglichkeiten ausführlicher aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="fb6a7-113">Kontotyp ist Projekt</span><span class="sxs-lookup"><span data-stu-id="fb6a7-113">Account type is Project</span></span>

<span data-ttu-id="fb6a7-114">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Projekt** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="fb6a7-115">Die folgende Abbildung zeigt die Regel.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-115">The following illustration shows the rule.</span></span> <span data-ttu-id="fb6a7-116">Folgende Punkte zeigen die möglichen Steuerarten für Projektkonten.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="fb6a7-117">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="fb6a7-118">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="fb6a7-119">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="fb6a7-120">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="fb6a7-121">Andernfalls ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="fb6a7-122">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-122">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Projektkonten](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="fb6a7-124">Der Kontentyp ist Kreditor.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-124">Account type is Vendor</span></span>

<span data-ttu-id="fb6a7-125">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Kreditor** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="fb6a7-126">Folgende Punkte zeigen die möglichen Steuerarten für Kreditorenkonten.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="fb6a7-127">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="fb6a7-128">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="fb6a7-129">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="fb6a7-130">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="fb6a7-131">Andernfalls ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="fb6a7-132">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-132">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Kreditorenkonten](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="fb6a7-134">Kontotyp ist Debitor</span><span class="sxs-lookup"><span data-stu-id="fb6a7-134">Account type is Customer</span></span>

<span data-ttu-id="fb6a7-135">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Debitor** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="fb6a7-136">Folgende Punkte zeigen die möglichen Steuerarten für Debitorenkonten.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="fb6a7-137">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="fb6a7-138">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="fb6a7-139">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="fb6a7-140">Andernfalls ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="fb6a7-141">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-141">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Debitorenkonten](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="fb6a7-143">Kontentyp ist Sachkonto</span><span class="sxs-lookup"><span data-stu-id="fb6a7-143">Account type is Ledger</span></span>

<span data-ttu-id="fb6a7-144">Die folgende Abbildung zeigt die Regel an, die angewendet werden soll, wenn nur ein Beleg Erfassungspositionen aufweist, in denen die Kontenart **Sachkonto** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="fb6a7-145">Folgende Punkte zeigen die möglichen Steuerarten für Sachkonten.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="fb6a7-146">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="fb6a7-147">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="fb6a7-148">Wenn der Erfassungsbetrag andernfalls Soll (positiv) ist, ist die Mehrwertsteuerart Vorsteuer; wenn der Erfassungsbetrag Gutschrift (negativ) ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="fb6a7-149">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-149">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Sachkonten](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="fb6a7-151">Überschreiben der Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="fb6a7-151">Override the sales tax direction</span></span>

<span data-ttu-id="fb6a7-152">Sie können die Mehrwertsteuerart überschreiben, wenn der Beleg nur Positionen enthält, in denen die Kontenart **Sachkonto** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="fb6a7-153">Navigieren Sie zu **Hauptbuch \> Kontenplan \> Konten \> Hauptkonten** und wählen Sie das Inforegister **Juristische Person überschreibt** aus.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="fb6a7-154">Ermitteln des Mehrwertsteuerbetrags</span><span class="sxs-lookup"><span data-stu-id="fb6a7-154">Determine the sales tax amount</span></span>

<span data-ttu-id="fb6a7-155">Dieser Abschnitt beschreibt, wie das Vorzeichen des Mehrwertsteuerbetrags berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Seite „Mehrwertsteuerbuchungen“](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="fb6a7-157">Die folgende Tabelle zeigt die generische Regel zum Bestimmen der Vorzeichen von Mehrwertsteuerbeträgen in der temporären Mehrwertsteuertabelle.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="fb6a7-158">Erfassungspositionbetrag</span><span class="sxs-lookup"><span data-stu-id="fb6a7-158">Journal line amount</span></span> | <span data-ttu-id="fb6a7-159">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="fb6a7-159">Sales tax direction</span></span>  | <span data-ttu-id="fb6a7-160">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="fb6a7-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="fb6a7-161">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-161">Positive</span></span>            | <span data-ttu-id="fb6a7-162">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-162">Sales Tax Receivable</span></span> | <span data-ttu-id="fb6a7-163">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-163">Positive</span></span>              |
| <span data-ttu-id="fb6a7-164">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-164">Positive</span></span>            | <span data-ttu-id="fb6a7-165">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-165">Sales Tax Payable</span></span>    | <span data-ttu-id="fb6a7-166">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-166">Negative</span></span>              |
| <span data-ttu-id="fb6a7-167">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-167">Negative</span></span>            | <span data-ttu-id="fb6a7-168">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-168">Sales Tax Receivable</span></span> | <span data-ttu-id="fb6a7-169">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-169">Negative</span></span>              |
| <span data-ttu-id="fb6a7-170">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-170">Negative</span></span>            | <span data-ttu-id="fb6a7-171">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-171">Sales Tax Payable</span></span>    | <span data-ttu-id="fb6a7-172">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-172">Positive</span></span>              |

<span data-ttu-id="fb6a7-173">Es gibt eine Sonderregelung für Belege, die nur Positionen **Projekt** oder **Sachkonto** besitzen, wenn eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe in der Position **Sachkonto** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="fb6a7-174">Diese Regel wird durch Aktivieren der unabhängigen Mehrwertsteuerberechnungsfunktion für allgemeine Erfassungen gesteuert.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="fb6a7-175">Wenn diese Funktion deaktiviert wird, verwendet der Steuerbetrag der **Sachkonto**-Position die Soll-/Kreditrichtung der Position **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="fb6a7-176">Wenn diese Funktion deaktiviert wird, verwendet der Steuerbetrag **Sachkonto**-Position seine eigene Soll-/Kreditrichtung.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="fb6a7-177">Die folgenden Tabellen zeigen die Regel für jedes Szenario an.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="fb6a7-178">**Regel, wenn die Funktion aktiviert ist.**</span><span class="sxs-lookup"><span data-stu-id="fb6a7-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="fb6a7-179">Erfassungspositionsbetrag des Projekts</span><span class="sxs-lookup"><span data-stu-id="fb6a7-179">Journal line amount of project</span></span> | <span data-ttu-id="fb6a7-180">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="fb6a7-180">Sales tax direction</span></span>  | <span data-ttu-id="fb6a7-181">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="fb6a7-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="fb6a7-182">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-182">Positive</span></span>                       | <span data-ttu-id="fb6a7-183">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-183">Sales Tax Receivable</span></span> | <span data-ttu-id="fb6a7-184">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-184">Positive</span></span>              |
| <span data-ttu-id="fb6a7-185">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-185">Negative</span></span>                       | <span data-ttu-id="fb6a7-186">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-186">Sales Tax Receivable</span></span> | <span data-ttu-id="fb6a7-187">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-187">Negative</span></span>              |

<span data-ttu-id="fb6a7-188">**Regel, wenn die Funktion deaktiviert ist.**</span><span class="sxs-lookup"><span data-stu-id="fb6a7-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="fb6a7-189">Erfassungspositionsbetrag des Sachkontos</span><span class="sxs-lookup"><span data-stu-id="fb6a7-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="fb6a7-190">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="fb6a7-190">Sales tax direction</span></span>  | <span data-ttu-id="fb6a7-191">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="fb6a7-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="fb6a7-192">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-192">Positive</span></span>                       | <span data-ttu-id="fb6a7-193">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-193">Sales Tax Receivable</span></span> | <span data-ttu-id="fb6a7-194">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-194">Positive</span></span>              |
| <span data-ttu-id="fb6a7-195">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-195">Negative</span></span>                       | <span data-ttu-id="fb6a7-196">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-196">Sales Tax Receivable</span></span> | <span data-ttu-id="fb6a7-197">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="fb6a7-198">Bestimmen des Mehrwertsteuerbetrags und des Kontos für den Beleg</span><span class="sxs-lookup"><span data-stu-id="fb6a7-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="fb6a7-199">Wenn Sie Mehrwertsteuern buchen, wird das Hauptkonto aus dem Sachkontobuchungsgruppenprofil abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="fb6a7-200">Wenn Mehrwertsteuer zu erstatten ist, verwendet das System das Konto für die Vorsteuer, das im Profil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="fb6a7-201">Wenn Mehrwertsteuer zu zahlen sind, verwendet das System das Konto für die Mehrwertsteuer, das im Profil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="fb6a7-202">Die allgemeine Regel wird in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="fb6a7-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="fb6a7-203">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="fb6a7-203">Sales tax direction</span></span>  | <span data-ttu-id="fb6a7-204">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="fb6a7-204">Sales tax amount sign</span></span> | <span data-ttu-id="fb6a7-205">Mehrwertsteuerkonto</span><span class="sxs-lookup"><span data-stu-id="fb6a7-205">Sales tax account</span></span>      | <span data-ttu-id="fb6a7-206">Belegbetrag</span><span class="sxs-lookup"><span data-stu-id="fb6a7-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="fb6a7-207">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-207">Sales Tax Receivable</span></span> | <span data-ttu-id="fb6a7-208">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-208">Positive</span></span>              | <span data-ttu-id="fb6a7-209">Vorsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="fb6a7-209">Tax Receivable Account</span></span> | <span data-ttu-id="fb6a7-210">Positiv (Soll)</span><span class="sxs-lookup"><span data-stu-id="fb6a7-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="fb6a7-211">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-211">Sales Tax Receivable</span></span> | <span data-ttu-id="fb6a7-212">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-212">Negative</span></span>              | <span data-ttu-id="fb6a7-213">Vorsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="fb6a7-213">Tax Receivable Account</span></span> | <span data-ttu-id="fb6a7-214">Negativ (Haben)</span><span class="sxs-lookup"><span data-stu-id="fb6a7-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="fb6a7-215">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-215">Sales Tax Payable</span></span>    | <span data-ttu-id="fb6a7-216">Positiv</span><span class="sxs-lookup"><span data-stu-id="fb6a7-216">Positive</span></span>              | <span data-ttu-id="fb6a7-217">Mehrwertsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="fb6a7-217">Tax Payable Account</span></span>    | <span data-ttu-id="fb6a7-218">Negativ (Haben)</span><span class="sxs-lookup"><span data-stu-id="fb6a7-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="fb6a7-219">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="fb6a7-219">Sales Tax Payable</span></span>    | <span data-ttu-id="fb6a7-220">Negativ</span><span class="sxs-lookup"><span data-stu-id="fb6a7-220">Negative</span></span>              | <span data-ttu-id="fb6a7-221">Mehrwertsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="fb6a7-221">Tax Payable Account</span></span>    | <span data-ttu-id="fb6a7-222">Positiv (Soll)</span><span class="sxs-lookup"><span data-stu-id="fb6a7-222">Positive (Debit)</span></span>  |
