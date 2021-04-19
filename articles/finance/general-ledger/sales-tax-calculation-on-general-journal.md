---
title: Mehrwertsteuerberechnung für allgemeine Erfassungspositionen
description: In diesem Thema wird erläutert, wie die Mehrwertsteuer für verschiedene Kontotypen (Kreditorenkonto, Debitorenkonto, Sachkonto und Projekt) in allgemeinen Erfassungspositionen berechnet werden.
author: EricWang
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: e4d367fe6cb729c9c5658a9bbbac04e53fdf9644
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815331"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="cc928-103">Mehrwertsteuerberechnung für allgemeine Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="cc928-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc928-104">In diesem Thema wird erläutert, wie die Mehrwertsteuer für verschiedene Kontotypen (Kreditorenkonto, Debitorenkonto, Sachkonto und Projekt) in allgemeinen Erfassungspositionen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="cc928-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="cc928-105">Der Prozess kann in drei Schritte unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="cc928-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="cc928-106">Ermitteln der Mehrwertsteuerart.</span><span class="sxs-lookup"><span data-stu-id="cc928-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="cc928-107">Festlegen des Mehrwertsteuerbetrags, der in einer temporären Mehrwertsteuertabelle gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="cc928-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="cc928-108">Bestimmen des Mehrwertsteuerbetrags und des Kontos für den Beleg.</span><span class="sxs-lookup"><span data-stu-id="cc928-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="cc928-109">Ermitteln der Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="cc928-109">Determine the sales tax direction</span></span>

<span data-ttu-id="cc928-110">Die Methode, mit der die Mehrwertsteuerart bestimmt wird, hängt von der Art des Kontos im Beleg ab.</span><span class="sxs-lookup"><span data-stu-id="cc928-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="cc928-111">Die Mehrwertsteuerart wird durch die Kombination aus Kontenart und Mehrwertsteuercodes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="cc928-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="cc928-112">In den folgenden Abschnitten sind die Möglichkeiten ausführlicher aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cc928-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="cc928-113">Kontotyp ist Projekt</span><span class="sxs-lookup"><span data-stu-id="cc928-113">Account type is Project</span></span>

<span data-ttu-id="cc928-114">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Projekt** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="cc928-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="cc928-115">Die folgende Abbildung zeigt die Regel.</span><span class="sxs-lookup"><span data-stu-id="cc928-115">The following illustration shows the rule.</span></span> <span data-ttu-id="cc928-116">Folgende Punkte zeigen die möglichen Steuerarten für Projektkonten.</span><span class="sxs-lookup"><span data-stu-id="cc928-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="cc928-117">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="cc928-118">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="cc928-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="cc928-119">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="cc928-120">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="cc928-121">Andernfalls ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="cc928-122">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="cc928-122">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Projektkonten](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="cc928-124">Der Kontentyp ist Kreditor.</span><span class="sxs-lookup"><span data-stu-id="cc928-124">Account type is Vendor</span></span>

<span data-ttu-id="cc928-125">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Kreditor** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="cc928-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="cc928-126">Folgende Punkte zeigen die möglichen Steuerarten für Kreditorenkonten.</span><span class="sxs-lookup"><span data-stu-id="cc928-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="cc928-127">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-127">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="cc928-128">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="cc928-128">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="cc928-129">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-129">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="cc928-130">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-130">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="cc928-131">Andernfalls ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-131">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="cc928-132">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="cc928-132">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Kreditorenkonten](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="cc928-134">Kontotyp ist Debitor</span><span class="sxs-lookup"><span data-stu-id="cc928-134">Account type is Customer</span></span>

<span data-ttu-id="cc928-135">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Debitor** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="cc928-135">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="cc928-136">Folgende Punkte zeigen die möglichen Steuerarten für Debitorenkonten.</span><span class="sxs-lookup"><span data-stu-id="cc928-136">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="cc928-137">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="cc928-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="cc928-138">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="cc928-139">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="cc928-140">Andernfalls ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-140">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="cc928-141">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="cc928-141">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Debitorenkonten](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="cc928-143">Kontentyp ist Sachkonto</span><span class="sxs-lookup"><span data-stu-id="cc928-143">Account type is Ledger</span></span>

<span data-ttu-id="cc928-144">Die folgende Abbildung zeigt die Regel an, die angewendet werden soll, wenn nur ein Beleg Erfassungspositionen aufweist, in denen die Kontenart **Sachkonto** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="cc928-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="cc928-145">Folgende Punkte zeigen die möglichen Steuerarten für Sachkonten.</span><span class="sxs-lookup"><span data-stu-id="cc928-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="cc928-146">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="cc928-147">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="cc928-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="cc928-148">Wenn der Erfassungsbetrag andernfalls Soll (positiv) ist, ist die Mehrwertsteuerart Vorsteuer; wenn der Erfassungsbetrag Gutschrift (negativ) ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="cc928-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="cc928-149">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="cc928-149">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Sachkonten](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="cc928-151">Überschreiben der Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="cc928-151">Override the sales tax direction</span></span>

<span data-ttu-id="cc928-152">Sie können die Mehrwertsteuerart überschreiben, wenn der Beleg nur Positionen enthält, in denen die Kontenart **Sachkonto** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="cc928-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="cc928-153">Navigieren Sie zu **Hauptbuch \> Kontenplan \> Konten \> Hauptkonten** und wählen Sie das Inforegister **Juristische Person überschreibt** aus.</span><span class="sxs-lookup"><span data-stu-id="cc928-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="cc928-154">Ermitteln des Mehrwertsteuerbetrags</span><span class="sxs-lookup"><span data-stu-id="cc928-154">Determine the sales tax amount</span></span>

<span data-ttu-id="cc928-155">Dieser Abschnitt beschreibt, wie das Vorzeichen des Mehrwertsteuerbetrags berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="cc928-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Seite „Mehrwertsteuerbuchungen“](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="cc928-157">Die folgende Tabelle zeigt die generische Regel zum Bestimmen der Vorzeichen von Mehrwertsteuerbeträgen in der temporären Mehrwertsteuertabelle.</span><span class="sxs-lookup"><span data-stu-id="cc928-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="cc928-158">Erfassungspositionbetrag</span><span class="sxs-lookup"><span data-stu-id="cc928-158">Journal line amount</span></span> | <span data-ttu-id="cc928-159">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="cc928-159">Sales tax direction</span></span>  | <span data-ttu-id="cc928-160">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="cc928-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="cc928-161">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-161">Positive</span></span>            | <span data-ttu-id="cc928-162">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-162">Sales Tax Receivable</span></span> | <span data-ttu-id="cc928-163">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-163">Positive</span></span>              |
| <span data-ttu-id="cc928-164">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-164">Positive</span></span>            | <span data-ttu-id="cc928-165">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-165">Sales Tax Payable</span></span>    | <span data-ttu-id="cc928-166">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-166">Negative</span></span>              |
| <span data-ttu-id="cc928-167">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-167">Negative</span></span>            | <span data-ttu-id="cc928-168">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-168">Sales Tax Receivable</span></span> | <span data-ttu-id="cc928-169">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-169">Negative</span></span>              |
| <span data-ttu-id="cc928-170">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-170">Negative</span></span>            | <span data-ttu-id="cc928-171">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-171">Sales Tax Payable</span></span>    | <span data-ttu-id="cc928-172">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-172">Positive</span></span>              |

<span data-ttu-id="cc928-173">Es gibt eine Sonderregelung für Belege, die nur Positionen **Projekt** oder **Sachkonto** besitzen, wenn eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe in der Position **Sachkonto** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="cc928-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="cc928-174">Diese Regel wird durch Aktivieren der unabhängigen Mehrwertsteuerberechnungsfunktion für allgemeine Erfassungen gesteuert.</span><span class="sxs-lookup"><span data-stu-id="cc928-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="cc928-175">Wenn diese Funktion deaktiviert wird, verwendet der Steuerbetrag der **Sachkonto**-Position die Soll-/Kreditrichtung der Position **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="cc928-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="cc928-176">Wenn diese Funktion deaktiviert wird, verwendet der Steuerbetrag **Sachkonto**-Position seine eigene Soll-/Kreditrichtung.</span><span class="sxs-lookup"><span data-stu-id="cc928-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="cc928-177">Die folgenden Tabellen zeigen die Regel für jedes Szenario an.</span><span class="sxs-lookup"><span data-stu-id="cc928-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="cc928-178">**Regel, wenn die Funktion aktiviert ist.**</span><span class="sxs-lookup"><span data-stu-id="cc928-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="cc928-179">Erfassungspositionsbetrag des Projekts</span><span class="sxs-lookup"><span data-stu-id="cc928-179">Journal line amount of project</span></span> | <span data-ttu-id="cc928-180">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="cc928-180">Sales tax direction</span></span>  | <span data-ttu-id="cc928-181">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="cc928-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="cc928-182">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-182">Positive</span></span>                       | <span data-ttu-id="cc928-183">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-183">Sales Tax Receivable</span></span> | <span data-ttu-id="cc928-184">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-184">Positive</span></span>              |
| <span data-ttu-id="cc928-185">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-185">Negative</span></span>                       | <span data-ttu-id="cc928-186">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-186">Sales Tax Receivable</span></span> | <span data-ttu-id="cc928-187">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-187">Negative</span></span>              |

<span data-ttu-id="cc928-188">**Regel, wenn die Funktion deaktiviert ist.**</span><span class="sxs-lookup"><span data-stu-id="cc928-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="cc928-189">Erfassungspositionsbetrag des Sachkontos</span><span class="sxs-lookup"><span data-stu-id="cc928-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="cc928-190">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="cc928-190">Sales tax direction</span></span>  | <span data-ttu-id="cc928-191">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="cc928-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="cc928-192">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-192">Positive</span></span>                       | <span data-ttu-id="cc928-193">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-193">Sales Tax Receivable</span></span> | <span data-ttu-id="cc928-194">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-194">Positive</span></span>              |
| <span data-ttu-id="cc928-195">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-195">Negative</span></span>                       | <span data-ttu-id="cc928-196">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-196">Sales Tax Receivable</span></span> | <span data-ttu-id="cc928-197">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="cc928-198">Bestimmen des Mehrwertsteuerbetrags und des Kontos für den Beleg</span><span class="sxs-lookup"><span data-stu-id="cc928-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="cc928-199">Wenn Sie Mehrwertsteuern buchen, wird das Hauptkonto aus dem Sachkontobuchungsgruppenprofil abgerufen.</span><span class="sxs-lookup"><span data-stu-id="cc928-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="cc928-200">Wenn Mehrwertsteuer zu erstatten ist, verwendet das System das Konto für die Vorsteuer, das im Profil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc928-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="cc928-201">Wenn Mehrwertsteuer zu zahlen sind, verwendet das System das Konto für die Mehrwertsteuer, das im Profil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="cc928-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="cc928-202">Die allgemeine Regel wird in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="cc928-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="cc928-203">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="cc928-203">Sales tax direction</span></span>  | <span data-ttu-id="cc928-204">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="cc928-204">Sales tax amount sign</span></span> | <span data-ttu-id="cc928-205">Mehrwertsteuerkonto</span><span class="sxs-lookup"><span data-stu-id="cc928-205">Sales tax account</span></span>      | <span data-ttu-id="cc928-206">Belegbetrag</span><span class="sxs-lookup"><span data-stu-id="cc928-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="cc928-207">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-207">Sales Tax Receivable</span></span> | <span data-ttu-id="cc928-208">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-208">Positive</span></span>              | <span data-ttu-id="cc928-209">Vorsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="cc928-209">Tax Receivable Account</span></span> | <span data-ttu-id="cc928-210">Positiv (Soll)</span><span class="sxs-lookup"><span data-stu-id="cc928-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="cc928-211">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-211">Sales Tax Receivable</span></span> | <span data-ttu-id="cc928-212">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-212">Negative</span></span>              | <span data-ttu-id="cc928-213">Vorsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="cc928-213">Tax Receivable Account</span></span> | <span data-ttu-id="cc928-214">Negativ (Haben)</span><span class="sxs-lookup"><span data-stu-id="cc928-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="cc928-215">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-215">Sales Tax Payable</span></span>    | <span data-ttu-id="cc928-216">Positiv</span><span class="sxs-lookup"><span data-stu-id="cc928-216">Positive</span></span>              | <span data-ttu-id="cc928-217">Mehrwertsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="cc928-217">Tax Payable Account</span></span>    | <span data-ttu-id="cc928-218">Negativ (Haben)</span><span class="sxs-lookup"><span data-stu-id="cc928-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="cc928-219">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="cc928-219">Sales Tax Payable</span></span>    | <span data-ttu-id="cc928-220">Negativ</span><span class="sxs-lookup"><span data-stu-id="cc928-220">Negative</span></span>              | <span data-ttu-id="cc928-221">Mehrwertsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="cc928-221">Tax Payable Account</span></span>    | <span data-ttu-id="cc928-222">Positiv (Soll)</span><span class="sxs-lookup"><span data-stu-id="cc928-222">Positive (Debit)</span></span>  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]