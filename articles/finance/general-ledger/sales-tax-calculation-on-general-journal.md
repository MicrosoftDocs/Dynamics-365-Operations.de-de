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
ms.openlocfilehash: dd1df355d39065d6959915cc916987d3c58b15a6
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570193"
---
# <a name="sales-tax-calculation-on-general-journal-lines"></a><span data-ttu-id="8fe86-103">Mehrwertsteuerberechnung für allgemeine Erfassungspositionen</span><span class="sxs-lookup"><span data-stu-id="8fe86-103">Sales tax calculation on general journal lines</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="8fe86-104">In diesem Thema wird erläutert, wie die Mehrwertsteuer für verschiedene Kontotypen (Kreditorenkonto, Debitorenkonto, Sachkonto und Projekt) in allgemeinen Erfassungspositionen berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="8fe86-104">This topic explains how sales taxes are calculated for different types of accounts (vendor, customer, ledger, and project) on general journal lines.</span></span>

<span data-ttu-id="8fe86-105">Der Prozess kann in drei Schritte unterteilt werden:</span><span class="sxs-lookup"><span data-stu-id="8fe86-105">The process can be divided into three steps:</span></span>

- <span data-ttu-id="8fe86-106">Ermitteln der Mehrwertsteuerart.</span><span class="sxs-lookup"><span data-stu-id="8fe86-106">Determine the sales tax direction.</span></span>

- <span data-ttu-id="8fe86-107">Festlegen des Mehrwertsteuerbetrags, der in einer temporären Mehrwertsteuertabelle gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="8fe86-107">Determine the sales tax amount that will be stored a temporary sales tax table.</span></span>

- <span data-ttu-id="8fe86-108">Bestimmen des Mehrwertsteuerbetrags und des Kontos für den Beleg.</span><span class="sxs-lookup"><span data-stu-id="8fe86-108">Determine the sales tax amount and account on the voucher.</span></span>

## <a name="determine-the-sales-tax-direction"></a><span data-ttu-id="8fe86-109">Ermitteln der Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="8fe86-109">Determine the sales tax direction</span></span>

<span data-ttu-id="8fe86-110">Die Methode, mit der die Mehrwertsteuerart bestimmt wird, hängt von der Art des Kontos im Beleg ab.</span><span class="sxs-lookup"><span data-stu-id="8fe86-110">The way that the sales tax direction is determined depends on the type of account in the voucher.</span></span> <span data-ttu-id="8fe86-111">Die Mehrwertsteuerart wird durch die Kombination aus Kontenart und Mehrwertsteuercodes bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8fe86-111">The sales tax direction is determined by the combination of account type and sales tax code.</span></span> <span data-ttu-id="8fe86-112">In den folgenden Abschnitten sind die Möglichkeiten ausführlicher aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8fe86-112">The following sections the possibilities in more detail.</span></span> 

### <a name="account-type-is-project"></a><span data-ttu-id="8fe86-113">Kontotyp ist Projekt</span><span class="sxs-lookup"><span data-stu-id="8fe86-113">Account type is Project</span></span>

<span data-ttu-id="8fe86-114">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Projekt** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="8fe86-114">If a voucher has journal line where the account type is **Project**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="8fe86-115">Die folgende Abbildung zeigt die Regel.</span><span class="sxs-lookup"><span data-stu-id="8fe86-115">The following illustration shows the rule.</span></span> <span data-ttu-id="8fe86-116">Folgende Punkte zeigen die möglichen Steuerarten für Projektkonten.</span><span class="sxs-lookup"><span data-stu-id="8fe86-116">The following points show the possible tax directions for project accounts.</span></span>

<span data-ttu-id="8fe86-117">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-117">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="8fe86-118">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="8fe86-118">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="8fe86-119">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-119">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8fe86-120">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-120">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8fe86-121">Andernfalls ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-121">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="8fe86-122">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="8fe86-122">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Projektkonten](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-vendor"></a><span data-ttu-id="8fe86-124">Der Kontentyp ist Kreditor.</span><span class="sxs-lookup"><span data-stu-id="8fe86-124">Account type is Vendor</span></span>

<span data-ttu-id="8fe86-125">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Kreditor** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="8fe86-125">If a voucher has journal line where the account type is **Vendor**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="8fe86-126">Folgende Punkte zeigen die möglichen Steuerarten für Kreditorenkonten.</span><span class="sxs-lookup"><span data-stu-id="8fe86-126">The following points show the possible tax directions for vendor accounts.</span></span> 

<span data-ttu-id="8fe86-127">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="8fe86-127">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="8fe86-128">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-128">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="8fe86-129">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-129">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Receivable.</span></span>


<span data-ttu-id="8fe86-130">Andernfalls ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-130">Otherwise, sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8fe86-131">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="8fe86-131">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Kreditorenkonten](media/Sales-Tax-Direction-Vendor.jpg)

### <a name="account-type-is-customer"></a><span data-ttu-id="8fe86-133">Kontotyp ist Debitor</span><span class="sxs-lookup"><span data-stu-id="8fe86-133">Account type is Customer</span></span>

<span data-ttu-id="8fe86-134">Wenn ein Beleg eine Erfassungsposition hat, in der die Kontenart **Debitor** ausgewählt ist, gilt für alle Erfassungspositionen im Beleg die gleiche Steuerart.</span><span class="sxs-lookup"><span data-stu-id="8fe86-134">If a voucher has journal line where the account type is **Customer**, all the journal lines in the voucher apply the same tax direction.</span></span> <span data-ttu-id="8fe86-135">Folgende Punkte zeigen die möglichen Steuerarten für Debitorenkonten.</span><span class="sxs-lookup"><span data-stu-id="8fe86-135">The following points show the possible tax directions for customer accounts.</span></span>

<span data-ttu-id="8fe86-136">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-136">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="8fe86-137">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="8fe86-137">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="8fe86-138">•   Wenn der Mehrwertsteuercode innergemeinschaftliche Mehrwertsteuer ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-138">•   If the sales tax code is intracom VAT, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8fe86-139">•   Wenn der Mehrwertsteuercode Verlagerung der Steuerschuld ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-139">•   If the sales tax code is reverse charge, then sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8fe86-140">Andernfalls ist die Mehrwertsteuerart Vorsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-140">Otherwise, sales tax direction is Sales Tax Receivable.</span></span>

<span data-ttu-id="8fe86-141">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="8fe86-141">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Debitorenkonten](media/Sales-Tax-Direction-Customer.jpg)

### <a name="account-type-is-ledger"></a><span data-ttu-id="8fe86-143">Kontentyp ist Sachkonto</span><span class="sxs-lookup"><span data-stu-id="8fe86-143">Account type is Ledger</span></span>

<span data-ttu-id="8fe86-144">Die folgende Abbildung zeigt die Regel an, die angewendet werden soll, wenn nur ein Beleg Erfassungspositionen aufweist, in denen die Kontenart **Sachkonto** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="8fe86-144">The following illustration shows the rule that applies when a voucher has only journal lines where the account type is **Ledger**.</span></span> <span data-ttu-id="8fe86-145">Folgende Punkte zeigen die möglichen Steuerarten für Sachkonten.</span><span class="sxs-lookup"><span data-stu-id="8fe86-145">The following points show the possible tax directions for ledger accounts.</span></span>

<span data-ttu-id="8fe86-146">•   Wenn der Mehrwertsteuercode Verbrauchssteuer ist, ist auch die Mehrwert-Steuerart Verbrauchssteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-146">•   If the sales tax code is use tax, then sales tax direction is Use Tax.</span></span>

<span data-ttu-id="8fe86-147">•   Wenn der Mehrwertsteuercode Steuerbefreiung ist, ist die Mehrwertsteuerart Steuerfreier Einkauf.</span><span class="sxs-lookup"><span data-stu-id="8fe86-147">•   If the sales tax code is exempt tax, then sales tax direction is Tax Free Purchase.</span></span>

<span data-ttu-id="8fe86-148">Wenn der Erfassungsbetrag andernfalls Soll (positiv) ist, ist die Mehrwertsteuerart Vorsteuer; wenn der Erfassungsbetrag Gutschrift (negativ) ist, ist die Mehrwertsteuerart Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="8fe86-148">Otherwise, if the journal amount is debit (positive) ,sales tax direction is Sales Tax Receivable; if the journal amount is credit (negative) ,sales tax direction is Sales Tax Payable.</span></span>

<span data-ttu-id="8fe86-149">Das folgende Diagramm veranschaulicht diese Regel grafisch.</span><span class="sxs-lookup"><span data-stu-id="8fe86-149">The following diagram illustrates the rule graphically.</span></span>

![Steuerartmöglichkeiten für Sachkonten](media/Sales-Tax-Direction-Ledger.jpg)

#### <a name="override-the-sales-tax-direction"></a><span data-ttu-id="8fe86-151">Überschreiben der Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="8fe86-151">Override the sales tax direction</span></span>

<span data-ttu-id="8fe86-152">Sie können die Mehrwertsteuerart überschreiben, wenn der Beleg nur Positionen enthält, in denen die Kontenart **Sachkonto** ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="8fe86-152">You can override the sales tax direction when the voucher contains only lines where the account type is **Ledger**.</span></span>

<span data-ttu-id="8fe86-153">Navigieren Sie zu **Hauptbuch \> Kontenplan \> Konten \> Hauptkonten** und wählen Sie das Inforegister **Juristische Person überschreibt** aus.</span><span class="sxs-lookup"><span data-stu-id="8fe86-153">Go to **General ledger \> Chart of accounts \> Accounts \> Main accounts**, and select the **Legal entity overrides** FastTab.</span></span>

## <a name="determine-the-sales-tax-amount"></a><span data-ttu-id="8fe86-154">Ermitteln des Mehrwertsteuerbetrags</span><span class="sxs-lookup"><span data-stu-id="8fe86-154">Determine the sales tax amount</span></span>

<span data-ttu-id="8fe86-155">Dieser Abschnitt beschreibt, wie das Vorzeichen des Mehrwertsteuerbetrags berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="8fe86-155">This section describes how the sales tax amount sign is calculated.</span></span>

![Seite „Mehrwertsteuerbuchungen“](media/sales-tax-amount-sign.jpg)

<span data-ttu-id="8fe86-157">Die folgende Tabelle zeigt die generische Regel zum Bestimmen der Vorzeichen von Mehrwertsteuerbeträgen in der temporären Mehrwertsteuertabelle.</span><span class="sxs-lookup"><span data-stu-id="8fe86-157">The following table shows the generic rule for determining the sign of sales tax amounts in the temporary sales tax table.</span></span>

| <span data-ttu-id="8fe86-158">Erfassungspositionbetrag</span><span class="sxs-lookup"><span data-stu-id="8fe86-158">Journal line amount</span></span> | <span data-ttu-id="8fe86-159">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="8fe86-159">Sales tax direction</span></span>  | <span data-ttu-id="8fe86-160">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="8fe86-160">Sales tax amount sign</span></span> |
|---------------------|----------------------|-----------------------|
| <span data-ttu-id="8fe86-161">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-161">Positive</span></span>            | <span data-ttu-id="8fe86-162">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-162">Sales Tax Receivable</span></span> | <span data-ttu-id="8fe86-163">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-163">Positive</span></span>              |
| <span data-ttu-id="8fe86-164">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-164">Positive</span></span>            | <span data-ttu-id="8fe86-165">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-165">Sales Tax Payable</span></span>    | <span data-ttu-id="8fe86-166">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-166">Negative</span></span>              |
| <span data-ttu-id="8fe86-167">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-167">Negative</span></span>            | <span data-ttu-id="8fe86-168">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-168">Sales Tax Receivable</span></span> | <span data-ttu-id="8fe86-169">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-169">Negative</span></span>              |
| <span data-ttu-id="8fe86-170">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-170">Negative</span></span>            | <span data-ttu-id="8fe86-171">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-171">Sales Tax Payable</span></span>    | <span data-ttu-id="8fe86-172">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-172">Positive</span></span>              |

<span data-ttu-id="8fe86-173">Es gibt eine Sonderregelung für Belege, die nur Positionen **Projekt** oder **Sachkonto** besitzen, wenn eine Mehrwertsteuergruppe und eine Artikel-Mehrwertsteuergruppe in der Position **Sachkonto** ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="8fe86-173">There is a special rule for vouchers that have only **Project** or **Ledger** lines, when a sales tax group or item sales tax group is selected on the **Ledger** line.</span></span> <span data-ttu-id="8fe86-174">Diese Regel wird durch Aktivieren der unabhängigen Mehrwertsteuerberechnungsfunktion für allgemeine Erfassungen gesteuert.</span><span class="sxs-lookup"><span data-stu-id="8fe86-174">This rule is controlled by Enable independent sales tax calculation feature for general journals.</span></span> <span data-ttu-id="8fe86-175">Wenn diese Funktion deaktiviert wird, verwendet der Steuerbetrag der **Sachkonto**-Position die Soll-/Kreditrichtung der Position **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="8fe86-175">When this feature is turned off, the tax amount of the **Ledger** line uses the debit/credit direction of the **Project** line.</span></span> <span data-ttu-id="8fe86-176">Wenn diese Funktion deaktiviert wird, verwendet der Steuerbetrag **Sachkonto**-Position seine eigene Soll-/Kreditrichtung.</span><span class="sxs-lookup"><span data-stu-id="8fe86-176">When the feature is turned on, the tax amount of the **Ledger** line uses its own debit/credit direction.</span></span> <span data-ttu-id="8fe86-177">Die folgenden Tabellen zeigen die Regel für jedes Szenario an.</span><span class="sxs-lookup"><span data-stu-id="8fe86-177">The following tables show the rule for each scenario.</span></span> 

<span data-ttu-id="8fe86-178">**Regel, wenn die Funktion aktiviert ist.**</span><span class="sxs-lookup"><span data-stu-id="8fe86-178">**Rule when the feature is turned on**</span></span>

| <span data-ttu-id="8fe86-179">Erfassungspositionsbetrag des Projekts</span><span class="sxs-lookup"><span data-stu-id="8fe86-179">Journal line amount of project</span></span> | <span data-ttu-id="8fe86-180">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="8fe86-180">Sales tax direction</span></span>  | <span data-ttu-id="8fe86-181">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="8fe86-181">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="8fe86-182">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-182">Positive</span></span>                       | <span data-ttu-id="8fe86-183">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-183">Sales Tax Receivable</span></span> | <span data-ttu-id="8fe86-184">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-184">Positive</span></span>              |
| <span data-ttu-id="8fe86-185">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-185">Negative</span></span>                       | <span data-ttu-id="8fe86-186">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-186">Sales Tax Receivable</span></span> | <span data-ttu-id="8fe86-187">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-187">Negative</span></span>              |

<span data-ttu-id="8fe86-188">**Regel, wenn die Funktion deaktiviert ist.**</span><span class="sxs-lookup"><span data-stu-id="8fe86-188">**Rule when the feature is turned off**</span></span>

| <span data-ttu-id="8fe86-189">Erfassungspositionsbetrag des Sachkontos</span><span class="sxs-lookup"><span data-stu-id="8fe86-189">Journal line amount of ledger</span></span>  | <span data-ttu-id="8fe86-190">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="8fe86-190">Sales tax direction</span></span>  | <span data-ttu-id="8fe86-191">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="8fe86-191">Sales tax amount sign</span></span> |
|--------------------------------|----------------------|-----------------------|
| <span data-ttu-id="8fe86-192">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-192">Positive</span></span>                       | <span data-ttu-id="8fe86-193">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-193">Sales Tax Receivable</span></span> | <span data-ttu-id="8fe86-194">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-194">Positive</span></span>              |
| <span data-ttu-id="8fe86-195">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-195">Negative</span></span>                       | <span data-ttu-id="8fe86-196">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-196">Sales Tax Receivable</span></span> | <span data-ttu-id="8fe86-197">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-197">Negative</span></span>              |

## <a name="determine-the-sales-tax-amount-and-account-on-the-voucher"></a><span data-ttu-id="8fe86-198">Bestimmen des Mehrwertsteuerbetrags und des Kontos für den Beleg</span><span class="sxs-lookup"><span data-stu-id="8fe86-198">Determine the sales tax amount and account on the voucher</span></span>

<span data-ttu-id="8fe86-199">Wenn Sie Mehrwertsteuern buchen, wird das Hauptkonto aus dem Sachkontobuchungsgruppenprofil abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8fe86-199">When you post sales taxes, the main account is retrieved from the ledger posting group profile.</span></span> <span data-ttu-id="8fe86-200">Wenn Mehrwertsteuer zu erstatten ist, verwendet das System das Konto für die Vorsteuer, das im Profil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8fe86-200">When sales taxes are receivable, the system uses the Sales Tax Receivable account that is specified in the profile.</span></span> <span data-ttu-id="8fe86-201">Wenn Mehrwertsteuer zu zahlen sind, verwendet das System das Konto für die Mehrwertsteuer, das im Profil angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8fe86-201">For sales taxes that are payable, the system uses Sales Tax Payable account that is specified in the profile.</span></span>

<span data-ttu-id="8fe86-202">Die allgemeine Regel wird in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="8fe86-202">The following table shows the generic rule.</span></span>

| <span data-ttu-id="8fe86-203">Mehrwertsteuerart</span><span class="sxs-lookup"><span data-stu-id="8fe86-203">Sales tax direction</span></span>  | <span data-ttu-id="8fe86-204">Mehrwertsteuerbetrag-Zeichen</span><span class="sxs-lookup"><span data-stu-id="8fe86-204">Sales tax amount sign</span></span> | <span data-ttu-id="8fe86-205">Mehrwertsteuerkonto</span><span class="sxs-lookup"><span data-stu-id="8fe86-205">Sales tax account</span></span>      | <span data-ttu-id="8fe86-206">Belegbetrag</span><span class="sxs-lookup"><span data-stu-id="8fe86-206">Amount on voucher</span></span> |
|----------------------|-----------------------|------------------------|-------------------|
| <span data-ttu-id="8fe86-207">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-207">Sales Tax Receivable</span></span> | <span data-ttu-id="8fe86-208">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-208">Positive</span></span>              | <span data-ttu-id="8fe86-209">Vorsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="8fe86-209">Tax Receivable Account</span></span> | <span data-ttu-id="8fe86-210">Positiv (Soll)</span><span class="sxs-lookup"><span data-stu-id="8fe86-210">Positive (Debit)</span></span>  |
| <span data-ttu-id="8fe86-211">Vorsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-211">Sales Tax Receivable</span></span> | <span data-ttu-id="8fe86-212">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-212">Negative</span></span>              | <span data-ttu-id="8fe86-213">Vorsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="8fe86-213">Tax Receivable Account</span></span> | <span data-ttu-id="8fe86-214">Negativ (Haben)</span><span class="sxs-lookup"><span data-stu-id="8fe86-214">Negative(Credit)</span></span>  |
| <span data-ttu-id="8fe86-215">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-215">Sales Tax Payable</span></span>    | <span data-ttu-id="8fe86-216">Positiv</span><span class="sxs-lookup"><span data-stu-id="8fe86-216">Positive</span></span>              | <span data-ttu-id="8fe86-217">Mehrwertsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="8fe86-217">Tax Payable Account</span></span>    | <span data-ttu-id="8fe86-218">Negativ (Haben)</span><span class="sxs-lookup"><span data-stu-id="8fe86-218">Negative(Credit)</span></span>  |
| <span data-ttu-id="8fe86-219">Mehrwertsteuer</span><span class="sxs-lookup"><span data-stu-id="8fe86-219">Sales Tax Payable</span></span>    | <span data-ttu-id="8fe86-220">Negativ</span><span class="sxs-lookup"><span data-stu-id="8fe86-220">Negative</span></span>              | <span data-ttu-id="8fe86-221">Mehrwertsteuerkonten</span><span class="sxs-lookup"><span data-stu-id="8fe86-221">Tax Payable Account</span></span>    | <span data-ttu-id="8fe86-222">Positiv (Soll)</span><span class="sxs-lookup"><span data-stu-id="8fe86-222">Positive (Debit)</span></span>  |
