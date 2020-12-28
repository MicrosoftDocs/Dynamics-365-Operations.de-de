---
title: Umsatzsteuererklärung für Deutschland
description: Dieses Thema enthält Informationen zum Generieren von QR-Rechnungen (QR-Slips) und zum Verarbeiten eingehender QR-Rechnungen.
author: v-lurodi
manager: AnnBe
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Germany
ms.author: v-lenest
ms.search.validFrom: 2019-06-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 089178474c44ce4efa3c74a4183e2a80b68d9303
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407756"
---
# <a name="vat-declaration-for-germany"></a><span data-ttu-id="18ff4-103">Umsatzsteuererklärung für Deutschland</span><span class="sxs-lookup"><span data-stu-id="18ff4-103">VAT declaration for Germany</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="18ff4-104">In diesem Thema wird erläutert, wie Sie die Mehrwertsteuererklärung für juristische Personen in Deutschland einrichten und erstellen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-104">This topic explains how to set up and generate the value-added tax (VAT) declaration for legal entities in Germany.</span></span>

<span data-ttu-id="18ff4-105">Weitere Informationen zur Einrichtung der Mehrwertsteuererklärung finden Sie unter [MwSt-Berichterstattung für Europa](emea-vat-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="18ff4-105">For general information about how to set up the VAT statement, see [VAT reporting for Europe](emea-vat-reporting.md).</span></span>

## <a name="set-up-sales-tax-reporting-codes-for-vat-reporting"></a><span data-ttu-id="18ff4-106">Mehrwertsteuer-Codes für Mehrwertsteuererklärung einrichten</span><span class="sxs-lookup"><span data-stu-id="18ff4-106">Set up sales tax reporting codes for VAT reporting</span></span>

<span data-ttu-id="18ff4-107">Richten Sie die Codes für die Mehrwertsteuererklärung ein, indem Sie die Anweisungen in [Mehrwertsteuer-Erklärungscodes einrichten](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-107">Set up sales tax reporting codes by following the instructions in [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).</span></span> <span data-ttu-id="18ff4-108">Die folgende Tabelle enthält ein Beispiel für Umsatzsteuer-Berichtscodes für Deutschland.</span><span class="sxs-lookup"><span data-stu-id="18ff4-108">The following table provides an example of sales tax reporting codes for Germany.</span></span>

<table width="614">
<thead>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-109"><strong>Code</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-109"><strong>Code</strong></span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-110"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-110"><strong>Description</strong></span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-111"><strong>Element in der XML-Datei der Umsatzsteuererklärung</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-111"><strong>Element in the XML file of the VAT declaration</strong></span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-112"><strong>Steuerbemessungsgrundlage oder Steuerbetrag</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-112"><strong>Tax base or tax amount</strong></span></span></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="18ff4-113"><strong>Steuerfreier Verkauf mit Vorsteuerabzug für innergemeinschaftliche Lieferungen (&sect; 4, Nr. 1b des UStG [Umsatzsteuergesetz</strong><strong></strong><strong>])</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-113"><strong>Tax-free sales with input tax deduction for intra-community supplies (&sect;4, no. 1, letter b of the UStG [Umsatzsteuergesetz</strong><strong>, or </strong><strong>VAT law])</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-114">41</span><span class="sxs-lookup"><span data-stu-id="18ff4-114">41</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-115">Innergemeinschaftlicher Versand (&sect;4, Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-115">Intra-community shipment (&sect;4, no.</span></span> <span data-ttu-id="18ff4-116">1b des UStG) für Kunden mit Steuerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="18ff4-116">1b of the UStG) to customers with tax registration.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-117">Kz41</span><span class="sxs-lookup"><span data-stu-id="18ff4-117">Kz41</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-118">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-118">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-119">44</span><span class="sxs-lookup"><span data-stu-id="18ff4-119">44</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-120">Innergemeinschaftliche Lieferungen von Neufahrzeugen an Kunden ohne Umsatzsteuer-Identifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="18ff4-120">Intra-community deliveries of new vehicles to customers without a VAT ID.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-121">Kz44</span><span class="sxs-lookup"><span data-stu-id="18ff4-121">Kz44</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-122">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-122">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-123">49</span><span class="sxs-lookup"><span data-stu-id="18ff4-123">49</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-124">Innergemeinschaftliche Lieferungen von Neufahrzeugen außerhalb eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="18ff4-124">Intra-community deliveries of new vehicles outside a company.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-125">Kz49</span><span class="sxs-lookup"><span data-stu-id="18ff4-125">Kz49</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-126">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-126">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-127">43</span><span class="sxs-lookup"><span data-stu-id="18ff4-127">43</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-128">Zusätzliche steuerfreie Verkäufe mit Vorsteuerabzug (z. B. Exporte).</span><span class="sxs-lookup"><span data-stu-id="18ff4-128">Additional tax-free sales with input tax deduction (for example, exports).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-129">Kz43</span><span class="sxs-lookup"><span data-stu-id="18ff4-129">Kz43</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-130">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-130">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="18ff4-131"><strong>Steuerfreie Verkäufe ohne Vorsteuerabzug (z. B. Verkäufe nach &sect;4, Nr. 8 bis 28 des UStG)</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-131"><strong>Tax-free sales without input tax deduction (for example, sales according to &sect;4, no. 8 through 28 of the UStG)</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-132">48</span><span class="sxs-lookup"><span data-stu-id="18ff4-132">48</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-133">Steuerfreier Verkauf ohne Vorsteuerabzug.</span><span class="sxs-lookup"><span data-stu-id="18ff4-133">Tax-free sales without input tax deduction.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-134">Kz48</span><span class="sxs-lookup"><span data-stu-id="18ff4-134">Kz48</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-135">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-135">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="18ff4-136"><strong>Steuerpflichtiger Umsatz</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-136"><strong>Taxable sales</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-137">81</span><span class="sxs-lookup"><span data-stu-id="18ff4-137">81</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-138">Steuerbemessungsgrundlage für Lieferungen oder Leistungen, die mit 19 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="18ff4-138">Tax base for deliveries or services that are charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-139">Kz81</span><span class="sxs-lookup"><span data-stu-id="18ff4-139">Kz81</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-140">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-140">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-141">181</span><span class="sxs-lookup"><span data-stu-id="18ff4-141">181</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-142">Steuerbetrag für Lieferungen oder Leistungen, die mit 19 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="18ff4-142">Tax amount for deliveries or services that are charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-143">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="18ff4-143">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-144">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-144">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-145">86</span><span class="sxs-lookup"><span data-stu-id="18ff4-145">86</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-146">Steuerbemessungsgrundlage für Lieferungen oder Leistungen, die mit 7 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="18ff4-146">Tax base for deliveries or services that are charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-147">Kz86</span><span class="sxs-lookup"><span data-stu-id="18ff4-147">Kz86</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-148">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-148">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-149">186</span><span class="sxs-lookup"><span data-stu-id="18ff4-149">186</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-150">Steuerbetrag für Lieferungen oder Leistungen, die mit 7 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="18ff4-150">Tax amount for deliveries or services that are charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-151">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="18ff4-151">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-152">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-152">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-153">35</span><span class="sxs-lookup"><span data-stu-id="18ff4-153">35</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-154">Steuerbemessungsgrundlage für Lieferungen oder Leistungen zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-154">Tax base for deliveries or services at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-155">Kz35</span><span class="sxs-lookup"><span data-stu-id="18ff4-155">Kz35</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-156">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-156">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-157">36</span><span class="sxs-lookup"><span data-stu-id="18ff4-157">36</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-158">Steuerbetrag für Lieferungen oder Leistungen zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-158">Tax amount for deliveries or services at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-159">Kz36</span><span class="sxs-lookup"><span data-stu-id="18ff4-159">Kz36</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-160">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-160">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-161">77</span><span class="sxs-lookup"><span data-stu-id="18ff4-161">77</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-162">Lieferungen von land- und forstwirtschaftlichen Betrieben nach &sect;24 des UStG an Kunden mit einer Umsatzsteuer-Identifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="18ff4-162">Deliveries of agricultural and forestry businesses, according to &sect;24 of the UStG, to customers who have a VAT ID.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-163">Kz77</span><span class="sxs-lookup"><span data-stu-id="18ff4-163">Kz77</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-164">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-164">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-165">76</span><span class="sxs-lookup"><span data-stu-id="18ff4-165">76</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-166">Steuerbemessungsgrundlage des Umsatzes, für den die Steuer zu zahlen ist &sect;24 des UStG (Sägewerksprodukte, Getränke und alkoholische Getränke wie Wein).</span><span class="sxs-lookup"><span data-stu-id="18ff4-166">Tax base of turnover that tax is payable for, according to &sect;24 of the UStG (sawmill products, beverages and alcoholic liquids, such as wine).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-167">Kz76</span><span class="sxs-lookup"><span data-stu-id="18ff4-167">Kz76</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-168">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-168">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-169">80</span><span class="sxs-lookup"><span data-stu-id="18ff4-169">80</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-170">Steuerbetrag des Umsatzes, für den die Steuer zu zahlen ist &sect;24 des UStG (Sägewerksprodukte, Getränke und alkoholische Getränke wie Wein).</span><span class="sxs-lookup"><span data-stu-id="18ff4-170">Tax amount of turnover that tax is payable for, according to &sect;24 of the UStG (sawmill products, beverages and alcoholic liquids, such as wine).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-171">Kz80</span><span class="sxs-lookup"><span data-stu-id="18ff4-171">Kz80</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-172">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-172">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="18ff4-173"><strong>Innergemeinschaftliche Akquisitionen und Mehrwertsteuer für solche Akquisitionen</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-173"><strong>Intra-community acquisitions and VAT payable for such acquisitions</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-174">91</span><span class="sxs-lookup"><span data-stu-id="18ff4-174">91</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-175">Steuerfreie innergemeinschaftliche Akquisitionen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-175">Tax-free intra-community acquisitions.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-176">Kz91</span><span class="sxs-lookup"><span data-stu-id="18ff4-176">Kz91</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-177">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-177">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-178">89</span><span class="sxs-lookup"><span data-stu-id="18ff4-178">89</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-179">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="18ff4-179">Tax base for the acquisition of goods from countries in the European Union (EU), charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-180">Kz89</span><span class="sxs-lookup"><span data-stu-id="18ff4-180">Kz89</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-181">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-181">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-182">189</span><span class="sxs-lookup"><span data-stu-id="18ff4-182">189</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-183">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="18ff4-183">Tax amount for the acquisition of goods from countries in the EU, charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-184">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="18ff4-184">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-185">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-185">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-186">93</span><span class="sxs-lookup"><span data-stu-id="18ff4-186">93</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-187">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="18ff4-187">Tax base for the acquisition of goods from countries in the EU, charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-188">Kz93</span><span class="sxs-lookup"><span data-stu-id="18ff4-188">Kz93</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-189">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-189">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-190">193</span><span class="sxs-lookup"><span data-stu-id="18ff4-190">193</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-191">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="18ff4-191">Tax amount for the acquisition of goods from countries in the EU, charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-192">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="18ff4-192">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-193">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-193">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-194">95</span><span class="sxs-lookup"><span data-stu-id="18ff4-194">95</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-195">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-195">Tax base for the acquisition of goods from countries in the EU at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-196">Kz95</span><span class="sxs-lookup"><span data-stu-id="18ff4-196">Kz95</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-197">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-197">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-198">98</span><span class="sxs-lookup"><span data-stu-id="18ff4-198">98</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-199">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-199">Tax amount for the acquisition of goods from countries in the EU at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-200">Kz98</span><span class="sxs-lookup"><span data-stu-id="18ff4-200">Kz98</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-201">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-201">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-202">94</span><span class="sxs-lookup"><span data-stu-id="18ff4-202">94</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-203">Steuerbemessungsgrundlage für innergemeinschaftliche Anschaffungen neuer Fahrzeuge (&sect;1b, Absätze 2 und 3 des UStG) von Lieferanten ohne MwSt.-ID zum allgemeinen Steuersatz.</span><span class="sxs-lookup"><span data-stu-id="18ff4-203">Tax base for intra-community acquisitions of new vehicles (&sect;1b, paragraphs 2 and 3 of the UStG) from suppliers without a VAT ID, at the general tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-204">Kz94</span><span class="sxs-lookup"><span data-stu-id="18ff4-204">Kz94</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-205">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-205">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-206">96</span><span class="sxs-lookup"><span data-stu-id="18ff4-206">96</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-207">Steuerbetrag für innergemeinschaftliche Anschaffungen neuer Fahrzeuge (&sect;1b, Absätze 2 und 3 des UStG) von Lieferanten ohne MwSt.-ID zum allgemeinen Steuersatz.</span><span class="sxs-lookup"><span data-stu-id="18ff4-207">Tax amount for intra-community acquisitions of new vehicles (&sect;1b, paragraphs 2 and 3 of the UStG) from suppliers without a VAT ID, at the general tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-208">Kz96</span><span class="sxs-lookup"><span data-stu-id="18ff4-208">Kz96</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-209">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-209">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="18ff4-210"><strong>Zusätzliche Informationen zum Vertrieb</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-210"><strong>Additional information about sales</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-211">42</span><span class="sxs-lookup"><span data-stu-id="18ff4-211">42</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-212">Lieferungen des ersten Kunden für gemeinschaftsinterne Dreieckstransaktionen (&sect;25b des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-212">Deliveries by the first customer for intra-community triangular transactions (&sect;25b of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-213">Kz42</span><span class="sxs-lookup"><span data-stu-id="18ff4-213">Kz42</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-214">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-214">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-215">60</span><span class="sxs-lookup"><span data-stu-id="18ff4-215">60</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-216">Steuerpflichtiger Umsatz des ausführenden Unternehmers, für den der Leistungsempfänger die Steuer schuldet, gemäß &sect;13b (5) des UStG.</span><span class="sxs-lookup"><span data-stu-id="18ff4-216">Taxable sales of the performing entrepreneur that the service recipient owes the tax for, according to &sect;13b (5) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-217">Kz60</span><span class="sxs-lookup"><span data-stu-id="18ff4-217">Kz60</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-218">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-218">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-219">21</span><span class="sxs-lookup"><span data-stu-id="18ff4-219">21</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-220">Sonstige nicht steuerpflichtige Dienstleistungen gemäß &sect;18b, Satz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-220">Other non-taxable services according to &sect;18b, sentence 1, no.</span></span> <span data-ttu-id="18ff4-221">2 des UStG.</span><span class="sxs-lookup"><span data-stu-id="18ff4-221">2 of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-222">Kz21</span><span class="sxs-lookup"><span data-stu-id="18ff4-222">Kz21</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-223">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-223">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-224">45</span><span class="sxs-lookup"><span data-stu-id="18ff4-224">45</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-225">Sonstige nicht steuerpflichtige Verkäufe (wenn der Erfüllungsort nicht in Deutschland liegt).</span><span class="sxs-lookup"><span data-stu-id="18ff4-225">Other non-taxable sales (where the place of performance isn't in Germany).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-226">Kz45</span><span class="sxs-lookup"><span data-stu-id="18ff4-226">Kz45</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-227">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-227">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="18ff4-228"><strong>Begünstigter als Steuerschuldner (&sect;13b des UStG)</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-228"><strong>Beneficiary as tax debtor (&sect;13b of the UStG)</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-229">46</span><span class="sxs-lookup"><span data-stu-id="18ff4-229">46</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-230">Steuerbemessungsgrundlage für sonstige Leistungen gemäß &sect;3A (2) UStG eines Unternehmers, der sich im Rest der Gemeinde befindet (&sect;13b (1) des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-230">Tax base for other services in accordance with &sect;3a (2) UStG of an entrepreneur that is located in the rest of the community (&sect;13b (1) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-231">Kz46</span><span class="sxs-lookup"><span data-stu-id="18ff4-231">Kz46</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-232">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-232">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-233">47</span><span class="sxs-lookup"><span data-stu-id="18ff4-233">47</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-234">Steuerbetrag für sonstige Leistungen gemäß &sect;3A (2) UStG eines Unternehmers, der sich im Rest der Gemeinde befindet (&sect;13b (1) des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-234">Tax amount for other services in accordance with &sect;3a (2) UStG of an entrepreneur that is located in the rest of the community (&sect;13b (1) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-235">Kz47</span><span class="sxs-lookup"><span data-stu-id="18ff4-235">Kz47</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-236">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-236">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-237">73</span><span class="sxs-lookup"><span data-stu-id="18ff4-237">73</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-238">Steuerbemessungsgrundlage des Umsatzes, der unter das Grundsteuergesetz fällt &ndash; insbesondere Lieferungen von Grundstücken, für die sich der ausführende Unternehmer für eine Steuerschuld gemäß &sect;9 (3) des UStG entschieden hat.</span><span class="sxs-lookup"><span data-stu-id="18ff4-238">Tax base of turnover that is covered by the property transfer tax law &ndash; in particular, deliveries of land for which the performing entrepreneur has opted for tax liability in accordance with &sect;9 (3) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-239">Kz73</span><span class="sxs-lookup"><span data-stu-id="18ff4-239">Kz73</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-240">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-240">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-241">74</span><span class="sxs-lookup"><span data-stu-id="18ff4-241">74</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-242">Steuerbetrag des Umsatzes, der unter das Grundsteuergesetz fällt &ndash; insbesondere Lieferungen von Grundstücken, für die sich der ausführende Unternehmer für eine Steuerschuld gemäß &sect;9 (3) des UStG entschieden hat.</span><span class="sxs-lookup"><span data-stu-id="18ff4-242">Tax amount of turnover that is covered by the property transfer tax law &ndash; in particular, deliveries of land for which the performing entrepreneur has opted for tax liability in accordance with &sect;9 (3) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-243">Kz74</span><span class="sxs-lookup"><span data-stu-id="18ff4-243">Kz74</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-244">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-244">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-245">84</span><span class="sxs-lookup"><span data-stu-id="18ff4-245">84</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-246">Steuerbemessungsgrundlage für andere Dienstleistungen (&sect;13b (2), Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-246">Tax base of other services (&sect;13b (2), no.</span></span> <span data-ttu-id="18ff4-247">1, 2 und 4 bis 11 des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-247">1, 2, and 4 through 11 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-248">Kz84</span><span class="sxs-lookup"><span data-stu-id="18ff4-248">Kz84</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-249">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="18ff4-249">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-250">85</span><span class="sxs-lookup"><span data-stu-id="18ff4-250">85</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-251">Steuerbetrag für andere Dienstleistungen (&sect;13b (2), Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-251">Tax amount of other services (&sect;13b (2), no.</span></span> <span data-ttu-id="18ff4-252">1, 2 und 4 bis 11 des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-252">1, 2, and 4 through 11 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-253">Kz85</span><span class="sxs-lookup"><span data-stu-id="18ff4-253">Kz85</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-254">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-254">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="18ff4-255"><strong>Abzugsfähige Vorsteuerbeträge</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-255"><strong>Deductible input tax amounts</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-256">66</span><span class="sxs-lookup"><span data-stu-id="18ff4-256">66</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-257">Steuer auf Eingaben aus Rechnungen anderer Unternehmen (&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-257">Tax on input from invoices of other companies (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="18ff4-258">1 des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-258">1 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-259">Kz66</span><span class="sxs-lookup"><span data-stu-id="18ff4-259">Kz66</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-260">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-260">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-261">61</span><span class="sxs-lookup"><span data-stu-id="18ff4-261">61</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-262">Vorsteuerbetrag aus innergemeinschaftlichen Erwerb von Gegenständen (&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-262">Input VAT amount from intra-community acquisitions of objects (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="18ff4-263">3 des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-263">3 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-264">Kz61</span><span class="sxs-lookup"><span data-stu-id="18ff4-264">Kz61</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-265">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-265">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-266">62</span><span class="sxs-lookup"><span data-stu-id="18ff4-266">62</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-267">Anfallender Umsatzsteuerimport(&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-267">Import sales tax that is incurred (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="18ff4-268">2 des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-268">2 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-269">Kz62</span><span class="sxs-lookup"><span data-stu-id="18ff4-269">Kz62</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-270">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-270">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-271">67</span><span class="sxs-lookup"><span data-stu-id="18ff4-271">67</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-272">Vorsteuerbeträge aus Dienstleistungen im Sinne von &sect;13b des UStG (&sect;15, Absatz 1, Klausel 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-272">Input tax amounts from services within the meaning of &sect;13b of the UStG (&sect;15, paragraph 1, clause 1, no.</span></span> <span data-ttu-id="18ff4-273">4 des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-273">4 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-274">Kz67</span><span class="sxs-lookup"><span data-stu-id="18ff4-274">Kz67</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-275">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-275">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-276">63</span><span class="sxs-lookup"><span data-stu-id="18ff4-276">63</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-277">Vorsteuerbeträge, die nach allgemeinen Durchschnittssätzen berechnet werden (&sect;23 und &sect;23A des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-277">Input tax amounts that are calculated according to general average rates (&sect;23 and &sect;23a of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-278">Kz63</span><span class="sxs-lookup"><span data-stu-id="18ff4-278">Kz63</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-279">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-279">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-280">64</span><span class="sxs-lookup"><span data-stu-id="18ff4-280">64</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-281">Korrektur des Vorsteuerabzugs (&sect;15A des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-281">Correction of input tax deduction (&sect;15a of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-282">Kz64</span><span class="sxs-lookup"><span data-stu-id="18ff4-282">Kz64</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-283">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-283">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-284">59</span><span class="sxs-lookup"><span data-stu-id="18ff4-284">59</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-285">Vorsteuerabzug für innergemeinschaftliche Lieferungen neuer Fahrzeuge außerhalb eines Unternehmens (&sect;2A des UStG) und Kleinunternehmen im Sinne von &sect;19 (1) des UStG (&sect;15 (4A) des UStG).</span><span class="sxs-lookup"><span data-stu-id="18ff4-285">Input tax deduction for intra-community deliveries of new vehicles outside a company (&sect;2a of the UStG) and small businesses within the meaning of &sect;19 (1) of the UStG (&sect;15 (4a) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-286">Kz59</span><span class="sxs-lookup"><span data-stu-id="18ff4-286">Kz59</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-287">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-287">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="18ff4-288"><strong>Sonstige Steuerbeträge</strong></span><span class="sxs-lookup"><span data-stu-id="18ff4-288"><strong>Other tax amounts</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-289">65</span><span class="sxs-lookup"><span data-stu-id="18ff4-289">65</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-290">Steuern aufgrund von Änderungen in der Form der Besteuerung und Nachsteuer auf besteuerte Anzahlungen usw. aufgrund von Änderungen des Steuersatzes.</span><span class="sxs-lookup"><span data-stu-id="18ff4-290">Tax because of changes in the form of taxation, and after-tax on taxed down payments, and so on, because of changes in tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-291">Kz65</span><span class="sxs-lookup"><span data-stu-id="18ff4-291">Kz65</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-292">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-292">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-293">69</span><span class="sxs-lookup"><span data-stu-id="18ff4-293">69</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-294">Steuerbeträge, die auf Rechnungen falsch oder unplausibel ausgewiesen sind (&sect;14c des UStG) sowie Steuerbeträge, die in Übereinstimmung mit &sect;6A (4), Satz 2; &sect;17 (1), Satz 6 und &sect;25b (2) des UStG <strong>geschuldet</strong> sind oder <strong>geschuldete Steuerbeträge</strong> von einem Outsourcer oder Lagerhalter gemäß &sect;13A (2) 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="18ff4-294">Tax amounts that are shown incorrectly or unjustifiably on invoices (&sect;14c of the UStG), and also tax amounts that are <strong>owed</strong> in accordance with &sect;6a (4), sentence 2; &sect;17 (1), sentence 6; and &sect;25b (2) of the UStG, or <strong>tax amounts that are owed</strong> by an outsourcer or warehouse keeper in accordance with &sect;13a (2) 1, no.</span></span> <span data-ttu-id="18ff4-295">6 des UStG.</span><span class="sxs-lookup"><span data-stu-id="18ff4-295">6 of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-296">Kz69</span><span class="sxs-lookup"><span data-stu-id="18ff4-296">Kz69</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-297">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-297">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-298">39</span><span class="sxs-lookup"><span data-stu-id="18ff4-298">39</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-299">Abzug der vereinbarten Sondervorauszahlung für eine langfristige Verlängerung (die in der Regel erst in der letzten Vorankündigung des Steuerzeitraums erfolgt).</span><span class="sxs-lookup"><span data-stu-id="18ff4-299">Deduction of the stipulated special advance payment for long-term extension (which usually will be completed only in the last advance notification of the taxation period).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-300">Kz39</span><span class="sxs-lookup"><span data-stu-id="18ff4-300">Kz39</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-301">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-301">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="18ff4-302">83</span><span class="sxs-lookup"><span data-stu-id="18ff4-302">83</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="18ff4-303">Gesamtbetrag der Mehrwertsteuer (Mehrwertsteuer-Vorauszahlung oder Mehrwertsteuerüberschuss).</span><span class="sxs-lookup"><span data-stu-id="18ff4-303">Total VAT amount (VAT advance payment or VAT surplus).</span></span></p>
<p><span data-ttu-id="18ff4-304">Bei der Umsatzsteuererklärung im XML-Format wird der Wert in diesem Feld automatisch als Summe der Berichtscodes 181, 186, 36, 80, 189, 193, 98, 96, 47, 74 und 85 abzüglich der Berichtscodes 66, 61, 62, 67, 63, 64, 59, 69 und 39 berechnet.</span><span class="sxs-lookup"><span data-stu-id="18ff4-304">On the VAT declaration in XML format, the value in this box is automatically calculated as the sum of reporting codes 181, 186, 36, 80, 189, 193, 98, 96, 47, 74, and 85, minus reporting codes 66, 61, 62, 67, 63, 64, 59, 69, and 39.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="18ff4-305">Kz83</span><span class="sxs-lookup"><span data-stu-id="18ff4-305">Kz83</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="18ff4-306">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="18ff4-306">Tax amount</span></span></p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>

> [!NOTE]
> <span data-ttu-id="18ff4-307">Beispiele für Formen von Mehrwertsteuererklärungen, die Deklarationszeilencodes enthalten, finden Sie unter [Formulare im Mehrwertsteuerverfahren für das Jahr 2020](https://umsatzsteuer-voranmeldung-2020.taxpool.net/Umsatzsteuer-Voranmeldung-2020.pdf).</span><span class="sxs-lookup"><span data-stu-id="18ff4-307">For sample forms of advance VAT returns that include declaration row codes, see [Forms in the VAT procedure for the year 2020](https://umsatzsteuer-voranmeldung-2020.taxpool.net/Umsatzsteuer-Voranmeldung-2020.pdf).</span></span>

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="18ff4-308">Mehrwertsteuercodes einrichten</span><span class="sxs-lookup"><span data-stu-id="18ff4-308">Set up sales tax codes</span></span>

<span data-ttu-id="18ff4-309">Richten Sie die Codes für die Mehrwertsteuererklärung ein, indem Sie die Anweisungen in [Mehrwertsteuercodes für MwSt-Berichterstattung](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) und [Mehrwertsteuerübersicht](../general-ledger/indirect-taxes-overview.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-309">Set up sales tax codes by following the instructions in [Sales tax codes for VAT reporting](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) and [Sales tax overview](../general-ledger/indirect-taxes-overview.md).</span></span>

> [!NOTE]
> <span data-ttu-id="18ff4-310">In einer deutschen juristischen Entität sollten Umsatzsteuerkennzeichen für steuerfreie Verkäufe nach folgenden Regeln eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="18ff4-310">In a German legal entity, sales tax codes for tax-free sales should be set up according to the following rules:</span></span>
>
> - <span data-ttu-id="18ff4-311">Der Steuersatz beträgt mehr als 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="18ff4-311">The tax rate is more than 0 (zero).</span></span>
> - <span data-ttu-id="18ff4-312">Das Steuerkennzeichen ist als **Befreit** auf der **Umsatzsteuergruppen**-Seite gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="18ff4-312">The tax code is marked as **Exempt** on the **Sales tax groups** page.</span></span>

## <a name="create-a-vat-declaration-in-xml-format"></a><a name= "createvatdecxmlformat"></a><span data-ttu-id="18ff4-313">Erstellen einer Umsatzsteuererklärung im XML-Format</span><span class="sxs-lookup"><span data-stu-id="18ff4-313">Create a VAT declaration in XML format</span></span>

1. <span data-ttu-id="18ff4-314">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in der **Bibliothek der freigegebenen Anlagen** laden Sie die neuesten Versionen der Konfigurationen für die elektronische Berichterstattung (ER) für das Format der Umsatzsteuererklärung herunter:</span><span class="sxs-lookup"><span data-stu-id="18ff4-314">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in the **Shared asset library**, download the latest versions of the Electronic reporting (ER) configurations for the VAT declaration format:</span></span>

    - <span data-ttu-id="18ff4-315">**Elster (DE)**</span><span class="sxs-lookup"><span data-stu-id="18ff4-315">**Elster (DE)**</span></span>

    <span data-ttu-id="18ff4-316">Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="18ff4-316">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

2. <span data-ttu-id="18ff4-317">Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer-Erklärungscodes**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-317">Go to **Tax** \> **Setup** \> **Sales tax** \> **Electronic tax declaration setup**.</span></span>
3. <span data-ttu-id="18ff4-318">Im Feld **Formatzuordnung** wählen Sie das Format **Elster (DE)** aus, das Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="18ff4-318">In the **Format mapping** field, select the **Elster (DE)** format that you downloaded earlier.</span></span>
4. <span data-ttu-id="18ff4-319">Wechseln Sie zu **Steuer \> Erklärungen \> Mehrwertsteuer \> Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-319">Go to **Tax \> Declarations \> Sales tax \> Report sales tax for settlement period**.</span></span>
5. <span data-ttu-id="18ff4-320">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="18ff4-320">In the **Report sales tax for settlement period** dialog box, set the following fields.</span></span>

| <span data-ttu-id="18ff4-321">**Feld**</span><span class="sxs-lookup"><span data-stu-id="18ff4-321">**Field**</span></span>                 | <span data-ttu-id="18ff4-322">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18ff4-322">**Description**</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ff4-323">Ausgleichsperiode</span><span class="sxs-lookup"><span data-stu-id="18ff4-323">Settlement period</span></span>         | <span data-ttu-id="18ff4-324">Wählen Sie den gewünschten Berichtszeitraum aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-324">Select the applicable reporting period.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="18ff4-325">Startdatum</span><span class="sxs-lookup"><span data-stu-id="18ff4-325">From date</span></span>                 | <span data-ttu-id="18ff4-326">Geben Sie das erste Datum des zu berechnenden Mehrwertsteuer-Abrechnungszeitraums an, um die Mehrwertsteuer zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-326">Enter the first date of the sales tax settlement period that sales tax should be calculated for.</span></span> <span data-ttu-id="18ff4-327">Dieser Wert entspricht dem Datum im Feld **Vom** auf der **Mehrwertsteuer-Abrechnungszeitraum**-Seite.</span><span class="sxs-lookup"><span data-stu-id="18ff4-327">This value corresponds to the date in the **From** field on the **Sales tax settlement periods** page.</span></span>                                                                                 |
| <span data-ttu-id="18ff4-328">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="18ff4-328">Transaction date</span></span>          | <span data-ttu-id="18ff4-329">Geben Sie das Datum an, für das die Mehrwertsteuererklärung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="18ff4-329">Enter the date when the sales tax report is calculated.</span></span> <span data-ttu-id="18ff4-330">Der aktuelle Wert ist das aktuelle Datum.</span><span class="sxs-lookup"><span data-stu-id="18ff4-330">The default value is the current date.</span></span> <span data-ttu-id="18ff4-331">Die Mehrwertsteuerzahlung wird für alle Buchungen berechnet, die im Abrechnungszeitraum gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="18ff4-331">The sales tax payment is calculated for all transactions that were posted during the settlement period.</span></span>                                                                                  |
| <span data-ttu-id="18ff4-332">Mehrwertsteuer, Zahlungsversion</span><span class="sxs-lookup"><span data-stu-id="18ff4-332">Sales tax payment version</span></span> | <span data-ttu-id="18ff4-333">Wählen Sie den Mehrwertsteuer-Ausgleichstyp.</span><span class="sxs-lookup"><span data-stu-id="18ff4-333">Select the type of sales tax settlement.</span></span> <span data-ttu-id="18ff4-334">Wenn diese Umsatzsteuerabrechnung die erste Umsatzsteuerabrechnung für den Zeitraum ist, wählen Sie **Original**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-334">If this sales tax settlement is the first sales tax settlement for the period, select **Original**.</span></span> <span data-ttu-id="18ff4-335">Wenn bereits eine Umsatzsteuerabrechnung generiert wurde, wählen Sie **Neueste Korrekturen**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-335">If a sales tax settlement has already been generated, select **Latest corrections**.</span></span> <span data-ttu-id="18ff4-336">Weitere Informationen finden Sie unter [Eine Mehrwertsteuerzahlung erstellen](../general-ledger/tasks/create-sales-tax-payment.md).</span><span class="sxs-lookup"><span data-stu-id="18ff4-336">For more information, see [Create a sales tax payment](../general-ledger/tasks/create-sales-tax-payment.md).</span></span> |

6. <span data-ttu-id="18ff4-337">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-337">Select **OK**.</span></span>
7. <span data-ttu-id="18ff4-338">Im Dialogfeld **Deutsche Mehrwertsteuererklärung** stellen Sie die folgenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="18ff4-338">In the **German sales tax report** dialog box, set the following fields.</span></span>

| <span data-ttu-id="18ff4-339">**Feld**</span><span class="sxs-lookup"><span data-stu-id="18ff4-339">**Field**</span></span>                      | <span data-ttu-id="18ff4-340">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18ff4-340">**Description**</span></span>                                                                                                                                                 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18ff4-341">Elektronisches Steuerdokument erstellen</span><span class="sxs-lookup"><span data-stu-id="18ff4-341">Create electronic tax document</span></span> | <span data-ttu-id="18ff4-342">Setzen Sie diese Option auf **Ja**, um ein elektronisches Dokument zu erstellen, das die Details des Berichts enthält.</span><span class="sxs-lookup"><span data-stu-id="18ff4-342">Set this option to **Yes** to create an electronic document that contains the details of the report.</span></span>                                                            |
| <span data-ttu-id="18ff4-343">Separat übermittelte Dokumente</span><span class="sxs-lookup"><span data-stu-id="18ff4-343">Documents submitted separately</span></span> | <span data-ttu-id="18ff4-344">Setzen Sie diese Option auf **Ja**, wenn der gedruckte Bericht nicht zusammen mit dem elektronischen Dokument eingereicht wird.</span><span class="sxs-lookup"><span data-stu-id="18ff4-344">Set this option to **Yes** if the printed report isn't submitted together with the electronic document.</span></span> <span data-ttu-id="18ff4-345">In der XML-Datei sollte der Code Kz22 den Wert **1** haben.</span><span class="sxs-lookup"><span data-stu-id="18ff4-345">In the XML file, code Kz22 should have the value **1**.</span></span> |

8. <span data-ttu-id="18ff4-346">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-346">Select **OK**.</span></span> <span data-ttu-id="18ff4-347">Auf der **Elektronisches Steuererklärungsprotokoll**-Seite (**Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**) wird eine neue Zeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="18ff4-347">A new line is created on the **Electronic tax declaration log** page (**Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**).</span></span>

![Seite „Protokoll der elektronischen Steuererklärung“](media/1_Electronic_tax_declaration_log.png)

## <a name="preview-the-xml-file"></a><span data-ttu-id="18ff4-349">Vorschau der XML-Datei</span><span class="sxs-lookup"><span data-stu-id="18ff4-349">Preview the XML file</span></span>

1. <span data-ttu-id="18ff4-350">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-350">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**.</span></span>
2. <span data-ttu-id="18ff4-351">Auf der Seite **Protokoll der elektronischen Steuererklärung**, wählen Sie die **Vorschau**-Registerkarte, um eine Vorschau der gemeldeten Werte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-351">On the **Electronic tax declaration log** page, select the **Preview** tab to preview the reported values.</span></span>
3. <span data-ttu-id="18ff4-352">Um die XML-Datei zur weiteren Übermittlung (außerhalb des Systems) zu überprüfen oder zu speichern, wählen Sie die Zeile auf der **Protokoll der elektronischen Steuererklärung**-Seite, und wählen Sie dann das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="18ff4-352">To review or save the XML file for further submission (outside of the system), select the line on the **Electronic tax declaration log** page, and then select the paper clip symbol in the upper-right corner.</span></span>
4. <span data-ttu-id="18ff4-353">Die **Handhabung von Dokumenten**-Seite erscheint und zeigt die generierte Datei.</span><span class="sxs-lookup"><span data-stu-id="18ff4-353">The **Document handling** page appears and shows the generated file.</span></span> <span data-ttu-id="18ff4-354">Wählen Sie **Öffnen** oben auf der Seite, um die Datei in der Anwendung zu öffnen, die der XML-Erweiterung in Ihrem System zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="18ff4-354">Select **Open** at the top of the page to open the file in the application that is associated with the .xml extension in your system.</span></span>

## <a name="submission-the-vat-declaration-to-elster"></a><span data-ttu-id="18ff4-355">Senden Sie die Umsatzsteuererklärung an ELSTER</span><span class="sxs-lookup"><span data-stu-id="18ff4-355">Submission the VAT declaration to ELSTER</span></span>

<span data-ttu-id="18ff4-356">ELSTER (Elektronische Steuererklärung) ist ein deutsches Online-Finanzamt, das vom Bundeszentralen Finanzamt für die Online-Einreichung von Steuererklärungen konzipiert wurde.</span><span class="sxs-lookup"><span data-stu-id="18ff4-356">ELSTER (Elektronische Steuererklärung, or electronic tax declaration) is a German online tax office system that was designed by the Federal Central Tax Office for online submission of tax declarations.</span></span>

<span data-ttu-id="18ff4-357">Im [Entwicklerbereich](https://www.elster.de/elsterweb/entwickler/infoseite/download_eric_28.) auf der ELSTER-Website finden Sie Beispiele, die zeigen, wie Entwickler mit ELSTER Rich Client (ERiC) interagieren können, um Mehrwertsteuererklärungen im XML-Dateiformat einzureichen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-357">The [Developers area](https://www.elster.de/elsterweb/entwickler/infoseite/download_eric_28.) of the ELSTER website provides examples that show how developers can interact with ELSTER Rich Client (ERiC) for the submission of VAT declarations in XML file format.</span></span> <span data-ttu-id="18ff4-358">Beispiele werden für C++, C\# und Java bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="18ff4-358">Examples are provided for C++, C\#, and Java.</span></span> <span data-ttu-id="18ff4-359">Um auf diesen Bereich der Website zugreifen zu können, müssen Sie [als Entwickler registriert](https://www.elster.de/elsterweb/registrierung-entwickler) sein.</span><span class="sxs-lookup"><span data-stu-id="18ff4-359">To access this area of the website, you must be [registered as a developer](https://www.elster.de/elsterweb/registrierung-entwickler).</span></span> <span data-ttu-id="18ff4-360">Ein Beispiel könnte Ihnen helfen, Ihre eigene ausführbare Datei zu erstellen, mit der Sie XML-Dateien über ERiC senden können.</span><span class="sxs-lookup"><span data-stu-id="18ff4-360">An example might help you create your own executable file that you can use to submit XML files via ERiC.</span></span> <span data-ttu-id="18ff4-361">Um eine ausführbare Datei zum Senden von XML-Dateien an ELSTER zu verwenden, müssen Sie ERiC Dynamics Link Libraries (DLLs) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-361">To use an executable file to submit XML files to ELSTER, you must download ERiC dynamics-link libraries (DLLs).</span></span>

<span data-ttu-id="18ff4-362">Weitere Informationen zu ERiC-Versionen finden Sie unter [ELSTER-Website](https://www.elster.de/elsterweb/entwickler/infoseite/eric).</span><span class="sxs-lookup"><span data-stu-id="18ff4-362">For more information about ERiC releases, see [ELSTER website](https://www.elster.de/elsterweb/entwickler/infoseite/eric).</span></span>

## <a name="example"></a><a name="example"></a> <span data-ttu-id="18ff4-363">Beispiel</span><span class="sxs-lookup"><span data-stu-id="18ff4-363">Example</span></span>

<span data-ttu-id="18ff4-364">Das folgende Beispiel zeigt, wie Sie Umsatzsteuerkennzeichen und Umsatzsteuerberichtscodes einrichten, Transaktionen buchen und die deutsche Umsatzsteuererklärung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="18ff4-364">The following example shows how you can set up sales tax codes and sales tax reporting codes, post transactions, and generate the German VAT declaration.</span></span>

1. <span data-ttu-id="18ff4-365">Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuercodes** und richten Sie die folgenden Umsatzsteuerkennzeichen ein.</span><span class="sxs-lookup"><span data-stu-id="18ff4-365">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**, and set up the following sales tax codes.</span></span>

| <span data-ttu-id="18ff4-366">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-366">**Sales tax code**</span></span> | <span data-ttu-id="18ff4-367">**Prozentsatz**</span><span class="sxs-lookup"><span data-stu-id="18ff4-367">**Percentage**</span></span> | <span data-ttu-id="18ff4-368">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="18ff4-368">**Description**</span></span>                                                                       |
|--------------------|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18ff4-369">VAT19</span><span class="sxs-lookup"><span data-stu-id="18ff4-369">VAT19</span></span>              | <span data-ttu-id="18ff4-370">19</span><span class="sxs-lookup"><span data-stu-id="18ff4-370">19</span></span>             | <span data-ttu-id="18ff4-371">Inlandsverkäufe mit einer Quote von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="18ff4-371">Domestic sales at a rate of 19 percent.</span></span>                                               |
| <span data-ttu-id="18ff4-372">VAT7</span><span class="sxs-lookup"><span data-stu-id="18ff4-372">VAT7</span></span>               | <span data-ttu-id="18ff4-373">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-373">7</span></span>              | <span data-ttu-id="18ff4-374">Inlandsverkäufe mit einer Quote von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="18ff4-374">Domestic sales at a rate of 7 percent.</span></span>                                                |
| <span data-ttu-id="18ff4-375">InVAT19</span><span class="sxs-lookup"><span data-stu-id="18ff4-375">InVAT19</span></span>            | <span data-ttu-id="18ff4-376">19</span><span class="sxs-lookup"><span data-stu-id="18ff4-376">19</span></span>             | <span data-ttu-id="18ff4-377">Inlandseinkäufe mit einer Quote von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="18ff4-377">Domestic purchases at a rate of 19 percent.</span></span>                                           |
| <span data-ttu-id="18ff4-378">InVAT7</span><span class="sxs-lookup"><span data-stu-id="18ff4-378">InVAT7</span></span>             | <span data-ttu-id="18ff4-379">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-379">7</span></span>              | <span data-ttu-id="18ff4-380">Inlandseinkäufe mit einer Quote von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="18ff4-380">Domestic purchases at a rate of 7 percent.</span></span>                                            |
| <span data-ttu-id="18ff4-381">EU19</span><span class="sxs-lookup"><span data-stu-id="18ff4-381">EU19</span></span>               | <span data-ttu-id="18ff4-382">19</span><span class="sxs-lookup"><span data-stu-id="18ff4-382">19</span></span>             | <span data-ttu-id="18ff4-383">EU-Einkäufe mit einer Quote von 19 Prozent, wobei die **Erwerbsteuer (USA)**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="18ff4-383">EU purchases at a rate of 19 percent, where the **Use tax** option is set to **Yes**.</span></span> |
| <span data-ttu-id="18ff4-384">EU7</span><span class="sxs-lookup"><span data-stu-id="18ff4-384">EU7</span></span>                | <span data-ttu-id="18ff4-385">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-385">7</span></span>              | <span data-ttu-id="18ff4-386">EU-Einkäufe mit einer Quote von 7 Prozent, wobei die **Erwerbsteuer (USA)**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="18ff4-386">EU purchases at a rate of 7 percent, where the **Use tax** option is set to **Yes**.</span></span>  |
| <span data-ttu-id="18ff4-387">EUS</span><span class="sxs-lookup"><span data-stu-id="18ff4-387">EUS</span></span>                | <span data-ttu-id="18ff4-388">19</span><span class="sxs-lookup"><span data-stu-id="18ff4-388">19</span></span>             | <span data-ttu-id="18ff4-389">EU-Verkäufe, bei denen die **Befreit**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="18ff4-389">EU sales where the **Exempt** option is set to **Yes**.</span></span>                               |
| <span data-ttu-id="18ff4-390">THIRD</span><span class="sxs-lookup"><span data-stu-id="18ff4-390">THIRD</span></span>              | <span data-ttu-id="18ff4-391">19</span><span class="sxs-lookup"><span data-stu-id="18ff4-391">19</span></span>             | <span data-ttu-id="18ff4-392">Exportverkäufe, bei denen die **Befreit**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="18ff4-392">Export sales where the **Exempt** option is set to **Yes**.</span></span>                           |

2. <span data-ttu-id="18ff4-393">Auf der **Mehrwertsteuercodes**-Seite weisen Sie auf dem Inforegister **Berichtseinstellungen** den Mehrwertsteuercodes Berichtscodes zu.</span><span class="sxs-lookup"><span data-stu-id="18ff4-393">On the **Sales tax codes** page, on the **Report setup** FastTab, assign reporting codes to sales tax codes.</span></span>

<span data-ttu-id="18ff4-394">Die folgende Tabelle zeigt, wie Sie die Mehrwertsteuer-Berichtscodes den Mehrwertsteuercodes zuweisen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-394">The following table shows how to assign the sales tax reporting codes to sales tax codes.</span></span>

| <span data-ttu-id="18ff4-395">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-395">**Sales tax code**</span></span> | <span data-ttu-id="18ff4-396">**Steuerpflichtiger Umsatz**</span><span class="sxs-lookup"><span data-stu-id="18ff4-396">**Taxable sales**</span></span> | <span data-ttu-id="18ff4-397">**Steuerfreier Verkauf**</span><span class="sxs-lookup"><span data-stu-id="18ff4-397">**Tax-free sale**</span></span> | <span data-ttu-id="18ff4-398">**Mehrwertsteuer**</span><span class="sxs-lookup"><span data-stu-id="18ff4-398">**Sales tax payable**</span></span> | <span data-ttu-id="18ff4-399">**Steuerpflichtige Einkäufe**</span><span class="sxs-lookup"><span data-stu-id="18ff4-399">**Taxable purchases**</span></span> | <span data-ttu-id="18ff4-400">**Vorsteuer**</span><span class="sxs-lookup"><span data-stu-id="18ff4-400">**Sales tax receivable**</span></span> | <span data-ttu-id="18ff4-401">**Steuerpflichtiger Import**</span><span class="sxs-lookup"><span data-stu-id="18ff4-401">**Taxable import**</span></span> | <span data-ttu-id="18ff4-402">**Erwerbsteuer (USA)**</span><span class="sxs-lookup"><span data-stu-id="18ff4-402">**Use tax**</span></span> | <span data-ttu-id="18ff4-403">**Erwerbsteuerausgleich**</span><span class="sxs-lookup"><span data-stu-id="18ff4-403">**Offset use tax**</span></span> |
|--------------------|-------------------|-------------------|-----------------------|-----------------------|--------------------------|--------------------|-------------|--------------------|
| <span data-ttu-id="18ff4-404">VAT19</span><span class="sxs-lookup"><span data-stu-id="18ff4-404">VAT19</span></span>              | <span data-ttu-id="18ff4-405">81</span><span class="sxs-lookup"><span data-stu-id="18ff4-405">81</span></span>                |                   | <span data-ttu-id="18ff4-406">181</span><span class="sxs-lookup"><span data-stu-id="18ff4-406">181</span></span>                   |                       |                          |                    |             |                    |
| <span data-ttu-id="18ff4-407">VAT7</span><span class="sxs-lookup"><span data-stu-id="18ff4-407">VAT7</span></span>               | <span data-ttu-id="18ff4-408">86</span><span class="sxs-lookup"><span data-stu-id="18ff4-408">86</span></span>                |                   | <span data-ttu-id="18ff4-409">186</span><span class="sxs-lookup"><span data-stu-id="18ff4-409">186</span></span>                   |                       |                          |                    |             |                    |
| <span data-ttu-id="18ff4-410">InVAT19</span><span class="sxs-lookup"><span data-stu-id="18ff4-410">InVAT19</span></span>            |                   |                   |                       |                       | <span data-ttu-id="18ff4-411">66</span><span class="sxs-lookup"><span data-stu-id="18ff4-411">66</span></span>                       |                    |             |                    |
| <span data-ttu-id="18ff4-412">InVAT7</span><span class="sxs-lookup"><span data-stu-id="18ff4-412">InVAT7</span></span>             |                   |                   |                       |                       | <span data-ttu-id="18ff4-413">66</span><span class="sxs-lookup"><span data-stu-id="18ff4-413">66</span></span>                       |                    |             |                    |
| <span data-ttu-id="18ff4-414">EU19</span><span class="sxs-lookup"><span data-stu-id="18ff4-414">EU19</span></span>               |                   |                   |                       |                       |                          | <span data-ttu-id="18ff4-415">89</span><span class="sxs-lookup"><span data-stu-id="18ff4-415">89</span></span>                 | <span data-ttu-id="18ff4-416">189</span><span class="sxs-lookup"><span data-stu-id="18ff4-416">189</span></span>         | <span data-ttu-id="18ff4-417">61</span><span class="sxs-lookup"><span data-stu-id="18ff4-417">61</span></span>                 |
| <span data-ttu-id="18ff4-418">EU7</span><span class="sxs-lookup"><span data-stu-id="18ff4-418">EU7</span></span>                |                   |                   |                       |                       |                          | <span data-ttu-id="18ff4-419">93</span><span class="sxs-lookup"><span data-stu-id="18ff4-419">93</span></span>                 | <span data-ttu-id="18ff4-420">193</span><span class="sxs-lookup"><span data-stu-id="18ff4-420">193</span></span>         | <span data-ttu-id="18ff4-421">61</span><span class="sxs-lookup"><span data-stu-id="18ff4-421">61</span></span>                 |
| <span data-ttu-id="18ff4-422">EUS</span><span class="sxs-lookup"><span data-stu-id="18ff4-422">EUS</span></span>                |                   | <span data-ttu-id="18ff4-423">41</span><span class="sxs-lookup"><span data-stu-id="18ff4-423">41</span></span>                |                       |                       |                          |                    |             |                    |
| <span data-ttu-id="18ff4-424">THIRD</span><span class="sxs-lookup"><span data-stu-id="18ff4-424">THIRD</span></span>              |                   | <span data-ttu-id="18ff4-425">43</span><span class="sxs-lookup"><span data-stu-id="18ff4-425">43</span></span>                |                       |                       |                          |                    |             |                    |

> [!NOTE]
> <span data-ttu-id="18ff4-426">Die vorhergehende Konfiguration ist nur ein Beispiel und hängt von der Struktur der Mehrwertsteuercodes ab, die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="18ff4-426">The preceding configuration is just an example and depends on the structure of the sales tax codes that are used.</span></span> <span data-ttu-id="18ff4-427">Damit Werte für die Mehrwertsteuererklärung berechnet und übertragen werde, müssen Sie für jeden Steuercode, der im Mehrwertsteuerzahlungsprozess verwendet wird, einen entsprechenden Mehrwertsteuer-Erklärungscode in einem oder mehreren Feldern der Registerkarte **Berichteinstellung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-427">If you want values to be calculated and transferred to the sales tax report, for each tax code that is used in the sales tax payment process, you must set a relevant sales tax reporting code in one or more fields on the **Report setup** FastTab.</span></span>

3. <span data-ttu-id="18ff4-428">Wechseln Sie zu **Steuer \> Einstellung \> Mehrwertsteuer \> Einrichtung der elektronischen Steuererklärung**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-428">Go to **Tax \> Setup \> Sales tax \> Electronic tax declaration setup**.</span></span>
4. <span data-ttu-id="18ff4-429">Im Feld **Formatzuordnung** wählen Sie das Format **Elster (DE)** aus, das Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="18ff4-429">In the **Format mapping** field, select the **Elster (DE)** format that you downloaded earlier.</span></span>
5. <span data-ttu-id="18ff4-430">Führen Sie die folgenden Buchungen aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-430">Post the following transactions.</span></span> <span data-ttu-id="18ff4-431">Informationen zu Kundenrechnungen finden Sie beispielsweise unter **Debitorenkonten** \> **Rechnungen** \> **Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-431">For example, for customer invoices, go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span> <span data-ttu-id="18ff4-432">Kreditorenrechnungen wechseln Sie zu **Kreditorenkonten \> Rechnungen \> Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-432">For vendor invoices, go to **Accounts payable \> Invoices \> Invoice journal**.</span></span>

| <span data-ttu-id="18ff4-433">**Datum**</span><span class="sxs-lookup"><span data-stu-id="18ff4-433">**Date**</span></span>        | <span data-ttu-id="18ff4-434">**Buchungstyp**</span><span class="sxs-lookup"><span data-stu-id="18ff4-434">**Transaction type**</span></span>      | <span data-ttu-id="18ff4-435">**Nettobetrag**</span><span class="sxs-lookup"><span data-stu-id="18ff4-435">**Amount net**</span></span> | <span data-ttu-id="18ff4-436">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="18ff4-436">**VAT amount**</span></span> | <span data-ttu-id="18ff4-437">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-437">**Sales tax code**</span></span> | <span data-ttu-id="18ff4-438">**Erwartete Steuerbemessungsgrundlage – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-438">**Expected tax base – reporting code**</span></span> | <span data-ttu-id="18ff4-439">**Erwarteter Steuerbemessungsbetrag – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-439">**Expected tax amount – reporting code**</span></span> |
|-----------------|---------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| <span data-ttu-id="18ff4-440">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="18ff4-440">January 1, 2020</span></span> | <span data-ttu-id="18ff4-441">Debitorenrechnung</span><span class="sxs-lookup"><span data-stu-id="18ff4-441">Customer invoice</span></span>          | <span data-ttu-id="18ff4-442">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-442">100</span></span>            | <span data-ttu-id="18ff4-443">19</span><span class="sxs-lookup"><span data-stu-id="18ff4-443">19</span></span>             | <span data-ttu-id="18ff4-444">VAT19</span><span class="sxs-lookup"><span data-stu-id="18ff4-444">VAT19</span></span>              | <span data-ttu-id="18ff4-445">81</span><span class="sxs-lookup"><span data-stu-id="18ff4-445">81</span></span>                                     | <span data-ttu-id="18ff4-446">181</span><span class="sxs-lookup"><span data-stu-id="18ff4-446">181</span></span>                                      |
| <span data-ttu-id="18ff4-447">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="18ff4-447">January 1, 2020</span></span> | <span data-ttu-id="18ff4-448">Kreditorenrechnung (EU)</span><span class="sxs-lookup"><span data-stu-id="18ff4-448">Vendor invoice (EU)</span></span>       | <span data-ttu-id="18ff4-449">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-449">100</span></span>            | <span data-ttu-id="18ff4-450">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-450">7</span></span>              | <span data-ttu-id="18ff4-451">EU7</span><span class="sxs-lookup"><span data-stu-id="18ff4-451">EU7</span></span>                | <span data-ttu-id="18ff4-452">93</span><span class="sxs-lookup"><span data-stu-id="18ff4-452">93</span></span>                                     | <span data-ttu-id="18ff4-453">193 – Steuerpflichtig 61 – Steuerabzug</span><span class="sxs-lookup"><span data-stu-id="18ff4-453">193 – Tax payable 61 – Tax deduction</span></span>     |
| <span data-ttu-id="18ff4-454">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="18ff4-454">January 1, 2020</span></span> | <span data-ttu-id="18ff4-455">Debitorenrechnung (EU)</span><span class="sxs-lookup"><span data-stu-id="18ff4-455">Customer invoice (EU)</span></span>     | <span data-ttu-id="18ff4-456">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-456">100</span></span>            | <span data-ttu-id="18ff4-457">0</span><span class="sxs-lookup"><span data-stu-id="18ff4-457">0</span></span>              | <span data-ttu-id="18ff4-458">EUS</span><span class="sxs-lookup"><span data-stu-id="18ff4-458">EUS</span></span>                | <span data-ttu-id="18ff4-459">41</span><span class="sxs-lookup"><span data-stu-id="18ff4-459">41</span></span>                                     | <span data-ttu-id="18ff4-460">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="18ff4-460">Not applicable</span></span>                           |
| <span data-ttu-id="18ff4-461">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="18ff4-461">January 1, 2020</span></span> | <span data-ttu-id="18ff4-462">Debitorenrechnung (Export)</span><span class="sxs-lookup"><span data-stu-id="18ff4-462">Customer invoice (export)</span></span> | <span data-ttu-id="18ff4-463">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-463">100</span></span>            | <span data-ttu-id="18ff4-464">0</span><span class="sxs-lookup"><span data-stu-id="18ff4-464">0</span></span>              | <span data-ttu-id="18ff4-465">THIRD</span><span class="sxs-lookup"><span data-stu-id="18ff4-465">THIRD</span></span>              | <span data-ttu-id="18ff4-466">43</span><span class="sxs-lookup"><span data-stu-id="18ff4-466">43</span></span>                                     | <span data-ttu-id="18ff4-467">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="18ff4-467">Not applicable</span></span>                           |

6. <span data-ttu-id="18ff4-468">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-468">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
7. <span data-ttu-id="18ff4-469">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder auf die angegebenen Werte ein.</span><span class="sxs-lookup"><span data-stu-id="18ff4-469">In the **Report sales tax for settlement period** dialog box, set the following fields to the specified values:</span></span>

    - <span data-ttu-id="18ff4-470">**Ausgleichsperiode:** Mo</span><span class="sxs-lookup"><span data-stu-id="18ff4-470">**Settlement period:** Mon</span></span>
    - <span data-ttu-id="18ff4-471">**Von Datum** = 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="18ff4-471">**From date:** 1/1/2020</span></span>

8. <span data-ttu-id="18ff4-472">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-472">Select **OK**.</span></span>
9. <span data-ttu-id="18ff4-473">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld wählen Sie das **Elektronisches Steuerdokument erstellen**-Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-473">In the **German sales tax report** dialog box, select the **Create electronic tax document** check box.</span></span>
10. <span data-ttu-id="18ff4-474">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-474">Select **OK**.</span></span>
11. <span data-ttu-id="18ff4-475">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**, und wählen Sie die erforderliche Position aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-475">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**, and select the required line.</span></span>
12. <span data-ttu-id="18ff4-476">Auf der **Protokoll der elektronischen Steuererklärung**-Seite, wählen Sie die **Allgemein**-Registerkarte und überprüfen die allgemeinen Informationen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-476">On the **Electronic tax declaration log** page, select the **General** tab, and review the general information.</span></span>

![Seite „Protokoll der elektronischen Steuererklärung“, Registerkarte „Allgemein“](media/2_Electronic_tax_declaration_log.png)

13. <span data-ttu-id="18ff4-478">Wählen Sie **Vorschau** aus, klicken Sie auf die Registerkarte und überprüfen Sie die gemeldeten Werte.</span><span class="sxs-lookup"><span data-stu-id="18ff4-478">Select the **Preview** tab, and review the reported values.</span></span>

![Vorschau des Protokolls der elektronischen Steuererklärung](media/3_Electronic_tax_declaration_log.png)

14. <span data-ttu-id="18ff4-480">Wählen Sie das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="18ff4-480">Select the paper clip symbol in the upper-right corner.</span></span>
15. <span data-ttu-id="18ff4-481">Wählen Sie **Öffnen** und überprüfen Sie die XML-Datei oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="18ff4-481">Select **Open** at the top of the page, and review the XML file.</span></span>

![XML-Datei](media/4_XML_file.png)

### <a name="correction-transactions"></a><span data-ttu-id="18ff4-483">Korrekturtransaktionen</span><span class="sxs-lookup"><span data-stu-id="18ff4-483">Correction transactions</span></span>

1.  <span data-ttu-id="18ff4-484">Wählen Sie eine neue Transaktion aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-484">Post a new transaction.</span></span> <span data-ttu-id="18ff4-485">Informationen zur Buchung einer Kundenrechnung finden Sie beispielsweise unter **Debitorenkonten** \> **Rechnungen** \> **Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-485">For example, to post a customer invoice, go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>

| <span data-ttu-id="18ff4-486">**Datum**</span><span class="sxs-lookup"><span data-stu-id="18ff4-486">**Date**</span></span>        | <span data-ttu-id="18ff4-487">**Buchungstyp**</span><span class="sxs-lookup"><span data-stu-id="18ff4-487">**Transaction type**</span></span>        | <span data-ttu-id="18ff4-488">**Nettobetrag**</span><span class="sxs-lookup"><span data-stu-id="18ff4-488">**Amount net**</span></span> | <span data-ttu-id="18ff4-489">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="18ff4-489">**VAT amount**</span></span> | <span data-ttu-id="18ff4-490">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-490">**Sales tax code**</span></span> | <span data-ttu-id="18ff4-491">**Erwartete Steuerbemessungsgrundlage – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-491">**Expected tax base – Reporting code**</span></span> | <span data-ttu-id="18ff4-492">**Erwarteter Steuerbemessungsbetrag – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-492">**Expected tax amount – Reporting code**</span></span> |
|-----------------|-----------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| <span data-ttu-id="18ff4-493">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="18ff4-493">January 1, 2020</span></span> | <span data-ttu-id="18ff4-494">Debitorenrechnung (Inland)</span><span class="sxs-lookup"><span data-stu-id="18ff4-494">Customer invoice (domestic)</span></span> | <span data-ttu-id="18ff4-495">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-495">100</span></span>            | <span data-ttu-id="18ff4-496">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-496">7</span></span>              | <span data-ttu-id="18ff4-497">VAT7</span><span class="sxs-lookup"><span data-stu-id="18ff4-497">VAT7</span></span>               | <span data-ttu-id="18ff4-498">86</span><span class="sxs-lookup"><span data-stu-id="18ff4-498">86</span></span>                                     | <span data-ttu-id="18ff4-499">186</span><span class="sxs-lookup"><span data-stu-id="18ff4-499">186</span></span>                                      |

2. <span data-ttu-id="18ff4-500">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-500">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
3. <span data-ttu-id="18ff4-501">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder auf die angegebenen Werte ein.</span><span class="sxs-lookup"><span data-stu-id="18ff4-501">In the **Report sales tax for settlement period** dialog box, set the following fields to the specified values:</span></span>

    - <span data-ttu-id="18ff4-502">**Ausgleichsperiode:** Mo</span><span class="sxs-lookup"><span data-stu-id="18ff4-502">**Settlement period:** Mon</span></span>
    - <span data-ttu-id="18ff4-503">**Von Datum** = 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="18ff4-503">**From date:** 1/1/2020</span></span>

4. <span data-ttu-id="18ff4-504">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-504">Select **OK**.</span></span>
5. <span data-ttu-id="18ff4-505">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld wählen Sie das **Elektronisches Steuerdokument erstellen**-Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-505">In the **German sales tax report** dialog box, select the **Create electronic tax document** check box.</span></span>
6. <span data-ttu-id="18ff4-506">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-506">Select **OK**.</span></span>
7. <span data-ttu-id="18ff4-507">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**, und wählen Sie die erforderliche Position aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-507">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**, and select the required line.</span></span>
8. <span data-ttu-id="18ff4-508">Wählen Sie **Vorschau** aus, klicken Sie auf die Registerkarte und überprüfen Sie die gemeldeten Werte.</span><span class="sxs-lookup"><span data-stu-id="18ff4-508">Select the **Preview** tab, and review the reported values.</span></span>

![Vorschau des Protokolls der elektronischen Steuererklärung](media/5_Electronic_tax_declaration_log.png)

<span data-ttu-id="18ff4-510">Beachten Sie, dass eine Korrekturtransaktion zur Erklärung in Codes **86** und **83** hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="18ff4-510">Note that a correction transaction is added to the declaration in codes **86** and **83**.</span></span>

9. <span data-ttu-id="18ff4-511">Wählen Sie das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="18ff4-511">Select the paper clip symbol in the upper-right corner.</span></span>
10. <span data-ttu-id="18ff4-512">Wählen Sie **Öffnen** und überprüfen Sie die XML-Datei oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="18ff4-512">Select **Open** at the top of the page, and review the XML file.</span></span>

![XML-Datei](media/6_XML_file.png)

<span data-ttu-id="18ff4-514">Beachten Sie, dass eine Korrekturtransaktion zur Erklärung in Codes **86** und **83** hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="18ff4-514">Note that a correction transaction is added to the declaration in codes **86** and **83**.</span></span>

## <a name="review-sales-tax-report-amounts"></a><span data-ttu-id="18ff4-515">Überprüfen Sie die Beträge des Umsatzsteuerberichts</span><span class="sxs-lookup"><span data-stu-id="18ff4-515">Review sales tax report amounts</span></span> 

<span data-ttu-id="18ff4-516">Sie können den Umsatzsteuerbetrag optional im SSRS-Bericht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-516">You can optionally review sales tax amount in SSRS report.</span></span>

### <a name="set-up-the-report-layout-for-sales-tax-authorities"></a><span data-ttu-id="18ff4-517">Richten Sie das Berichtslayout für die Umsatzsteuerbehörden ein</span><span class="sxs-lookup"><span data-stu-id="18ff4-517">Set up the report layout for sales tax authorities</span></span>

1. <span data-ttu-id="18ff4-518">Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuerbehörden**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-518">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax authorities**.</span></span>
2. <span data-ttu-id="18ff4-519">Wählen Sie auf der Seite **Mehrwertsteuer-Behörden** die Mehrwertsteuerbehörde, die für den Mehrwertsteuer-Abrechnungszeitraum in den Mehrwertsteuercodes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="18ff4-519">On the **Sales tax authorities** page, select the sales tax authority that will be used in the sales tax codes for the sales tax settlement period.</span></span>
3. <span data-ttu-id="18ff4-520">Im **Berichtslayout**-Feld wählen Sie **Deutsches Steuererklärungslayout**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-520">In the **Report layout** field, select **German report layout**.</span></span>

### <a name="generate-a-sales-tax-payment-and-print-the-german-sales-tax-report"></a><a name="generatesalestaxpayment"></a> <span data-ttu-id="18ff4-521">Generieren Sie eine Mehrwertsteuerzahlung und drucken Sie den deutschen Mehrwertsteuerbericht aus</span><span class="sxs-lookup"><span data-stu-id="18ff4-521">Generate a sales tax payment and print the German sales tax report</span></span>

<span data-ttu-id="18ff4-522">Berechnen Sie am Ende des MwSt.-Berichtszeitraums die Mehrwertsteuerbeträge für den Abrechnungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="18ff4-522">At the end of the VAT reporting period, calculate the sales tax amounts for the settlement period.</span></span>

1. <span data-ttu-id="18ff4-523">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-523">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
2. <span data-ttu-id="18ff4-524">Im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld stellen die erforderlichen Felder wie [vorhin](#createvatdecxmlformat) beschrieben ein.</span><span class="sxs-lookup"><span data-stu-id="18ff4-524">In the **Settle and post sales tax** dialog box, set the required fields as described [earlier](#createvatdecxmlformat).</span></span>
3. <span data-ttu-id="18ff4-525">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-525">Select **OK**.</span></span>
4. <span data-ttu-id="18ff4-526">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld legen Sie die **Elektronisches Steuerdokument erstellen**-Option auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="18ff4-526">In the **German sales tax report** dialog box, set the **Create electronic tax document** option to **No**.</span></span>
5. <span data-ttu-id="18ff4-527">Wählen Sie **OK** aus, um die Mehrwertsteuerzahlung zu generieren und den Bericht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-527">Select **OK** to generate the sales tax payment and review the report.</span></span>

<span data-ttu-id="18ff4-528">Wenn Sie Transaktionen wie in Schritt 5 des [Beispiels](#example) zu Beginn dieses Themas buchen, werden die folgenden Daten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="18ff4-528">If you post transactions as described in step 5 of the [example](#example) earlier in this topic, you will see the following data.</span></span>

![Generierter deutscher Mehrwertsteuerbericht, Seite 1](media/7_Sales_tax_reporting.png)

![Generierter deutscher Mehrwertsteuerbericht, Seite 2](media/8_Sales_tax_reporting.png)

### <a name="print-a-sales-tax-payment-report-from-a-sales-tax-payment"></a><span data-ttu-id="18ff4-531">Drucken Sie einen Mehrwertsteuerzahlungsbericht aus einer Mehrwertsteuerzahlung</span><span class="sxs-lookup"><span data-stu-id="18ff4-531">Print a sales tax payment report from a sales tax payment</span></span>

1. <span data-ttu-id="18ff4-532">Wechseln Sie zu **Steuer** \> **Anfragen und Berichte** \> **Mehrwertsteuerzahlungen**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-532">Go to **Tax** \> **Inquiries and reports** \> **Sales tax payments**.</span></span>
2. <span data-ttu-id="18ff4-533">Auf der **Mehrwertsteuerzahlung**-Seite wählen Sie den Datensatz aus und wählen dann **Bericht drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-533">On the **Sales tax payment** page, select the record, and then select **Print report**.</span></span>
3. <span data-ttu-id="18ff4-534">Stellen Sie im Dialogfeld die Felder wie im vorherigen Abschnitt beschrieben ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-534">In the dialog box, set the fields as described in the previous section, and then select **OK**.</span></span>

### <a name="report-sales-tax-for-the-settlement-period"></a><span data-ttu-id="18ff4-535">Umsatzsteuer für Abrechnungszeitraum melden</span><span class="sxs-lookup"><span data-stu-id="18ff4-535">Report sales tax for the settlement period</span></span>

<span data-ttu-id="18ff4-536">Sie können den deutschen Mehrwertsteuerbericht auch mit der **Umsatzsteuer für Abrechnungszeitraum melden**-Anfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-536">You can also generate the German sales tax report by using the **Report sales tax for settlement period** inquiry.</span></span>

1. <span data-ttu-id="18ff4-537">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-537">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
2. <span data-ttu-id="18ff4-538">Im **Umsatzsteuer für Abrechnungszeitraum melden**-Dialogfeld, stellen Sie die **Ausgleichsperiode** und die **Anfangsdatum**-Felder wie im Abschnitt [Generieren Sie eine Mehrwertsteuerzahlung und drucken Sie den deutschen Mehrwertsteuerbericht aus](#generatesalestaxpayment) weiter oben in diesem Thema beschrieben ein.</span><span class="sxs-lookup"><span data-stu-id="18ff4-538">In the **Report sales tax for settlement period** dialog box, set the **Settlement period** and **From date** fields as described in the [Generate a sales tax payment and print the German sales tax report](#generatesalestaxpayment) section earlier in this topic.</span></span>
3. <span data-ttu-id="18ff4-539">Wählen Sie im Feld **Mehrwertsteuer, Zahlungsversion** einen der folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="18ff4-539">In the **Sales tax payment version** field, select one of the following values:</span></span>

- <span data-ttu-id="18ff4-540">**Original** – Einen Mehrwertsteuerbericht generieren für die erste gebuchte Ausgleichsberechnung für das Periodenintervall.</span><span class="sxs-lookup"><span data-stu-id="18ff4-540">**Original** – Generate a report for sales tax transactions of the first posted settlement calculation for the period.</span></span>
- <span data-ttu-id="18ff4-541">**Korrekturen** – Einen Mehrwertsteuerbericht generieren für nachfolgende Ausgleichsberechnungen für das Periodenintervall.</span><span class="sxs-lookup"><span data-stu-id="18ff4-541">**Corrections** – Generate a report for sales tax transactions of subsequent settlement calculations for the period.</span></span>
- <span data-ttu-id="18ff4-542">**Gesamtliste** – Erstellen Sie einen Bericht für alle Verkaufstransaktionen für den Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="18ff4-542">**Total list** – Generate a report for all sales transactions for the period.</span></span> <span data-ttu-id="18ff4-543">Diese Transaktionen umfassen ursprüngliche und korrigierte Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="18ff4-543">These transactions include original and corrected transactions.</span></span>

4. <span data-ttu-id="18ff4-544">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-544">Select **OK**.</span></span>
5. <span data-ttu-id="18ff4-545">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-545">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
6. <span data-ttu-id="18ff4-546">Wählen Sie im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Original** aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-546">In the **Settle and post sales tax** dialog box, in the **Sales tax payment version** field, select **Original**.</span></span>
7.  <span data-ttu-id="18ff4-547">Drucken Sie den Bericht aus und überprüfen Sie die Daten.</span><span class="sxs-lookup"><span data-stu-id="18ff4-547">Print the report, and review the data.</span></span>

| <span data-ttu-id="18ff4-548">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-548">**Reporting code**</span></span> | <span data-ttu-id="18ff4-549">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="18ff4-549">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="18ff4-550">41</span><span class="sxs-lookup"><span data-stu-id="18ff4-550">41</span></span>                 | <span data-ttu-id="18ff4-551">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-551">100</span></span>                  |
| <span data-ttu-id="18ff4-552">43</span><span class="sxs-lookup"><span data-stu-id="18ff4-552">43</span></span>                 | <span data-ttu-id="18ff4-553">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-553">100</span></span>                  |
| <span data-ttu-id="18ff4-554">61</span><span class="sxs-lookup"><span data-stu-id="18ff4-554">61</span></span>                 | <span data-ttu-id="18ff4-555">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-555">7</span></span>                    |
| <span data-ttu-id="18ff4-556">81</span><span class="sxs-lookup"><span data-stu-id="18ff4-556">81</span></span>                 | <span data-ttu-id="18ff4-557">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-557">100</span></span>                  |
| <span data-ttu-id="18ff4-558">93</span><span class="sxs-lookup"><span data-stu-id="18ff4-558">93</span></span>                 | <span data-ttu-id="18ff4-559">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-559">100</span></span>                  |
| <span data-ttu-id="18ff4-560">181</span><span class="sxs-lookup"><span data-stu-id="18ff4-560">181</span></span>                | <span data-ttu-id="18ff4-561">19</span><span class="sxs-lookup"><span data-stu-id="18ff4-561">19</span></span>                   |
| <span data-ttu-id="18ff4-562">193</span><span class="sxs-lookup"><span data-stu-id="18ff4-562">193</span></span>                | <span data-ttu-id="18ff4-563">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-563">7</span></span>                    |

8. <span data-ttu-id="18ff4-564">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-564">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
9. <span data-ttu-id="18ff4-565">Wählen Sie im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Neueste Korrekturen** aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-565">In the **Settle and post sales tax** dialog box, in the **Sales tax payment version** field, select **Latest corrections**.</span></span>
10. <span data-ttu-id="18ff4-566">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-566">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
11. <span data-ttu-id="18ff4-567">Wählen Sie im **Mehrwertsteuer für Abrechnungszeitraum melden**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Korrekturen** aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-567">In the **Report sales tax for settlement period** dialog box, in the **Sales tax payment version** field, select **Corrections**.</span></span> <span data-ttu-id="18ff4-568">Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="18ff4-568">The following table shows the result.</span></span>

| <span data-ttu-id="18ff4-569">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-569">**Reporting code**</span></span> | <span data-ttu-id="18ff4-570">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="18ff4-570">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="18ff4-571">86</span><span class="sxs-lookup"><span data-stu-id="18ff4-571">86</span></span>                 | <span data-ttu-id="18ff4-572">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-572">100</span></span>                  |
| <span data-ttu-id="18ff4-573">186</span><span class="sxs-lookup"><span data-stu-id="18ff4-573">186</span></span>                | <span data-ttu-id="18ff4-574">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-574">7</span></span>                    |

12. <span data-ttu-id="18ff4-575">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="18ff4-575">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
13. <span data-ttu-id="18ff4-576">Wählen Sie im **Mehrwertsteuer für Abrechnungszeitraum melden**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Gesamtliste** aus.</span><span class="sxs-lookup"><span data-stu-id="18ff4-576">In the **Report sales tax for settlement period** dialog box, in the **Sales tax payment version** field, select **Total list**.</span></span> <span data-ttu-id="18ff4-577">Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="18ff4-577">The following table shows the result.</span></span>

| <span data-ttu-id="18ff4-578">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="18ff4-578">**Reporting code**</span></span> | <span data-ttu-id="18ff4-579">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="18ff4-579">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="18ff4-580">41</span><span class="sxs-lookup"><span data-stu-id="18ff4-580">41</span></span>                 | <span data-ttu-id="18ff4-581">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-581">100</span></span>                  |
| <span data-ttu-id="18ff4-582">43</span><span class="sxs-lookup"><span data-stu-id="18ff4-582">43</span></span>                 | <span data-ttu-id="18ff4-583">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-583">100</span></span>                  |
| <span data-ttu-id="18ff4-584">61</span><span class="sxs-lookup"><span data-stu-id="18ff4-584">61</span></span>                 | <span data-ttu-id="18ff4-585">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-585">7</span></span>                    |
| <span data-ttu-id="18ff4-586">81</span><span class="sxs-lookup"><span data-stu-id="18ff4-586">81</span></span>                 | <span data-ttu-id="18ff4-587">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-587">100</span></span>                  |
| <span data-ttu-id="18ff4-588">86</span><span class="sxs-lookup"><span data-stu-id="18ff4-588">86</span></span>                 | <span data-ttu-id="18ff4-589">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-589">100</span></span>                  |
| <span data-ttu-id="18ff4-590">93</span><span class="sxs-lookup"><span data-stu-id="18ff4-590">93</span></span>                 | <span data-ttu-id="18ff4-591">100</span><span class="sxs-lookup"><span data-stu-id="18ff4-591">100</span></span>                  |
| <span data-ttu-id="18ff4-592">181</span><span class="sxs-lookup"><span data-stu-id="18ff4-592">181</span></span>                | <span data-ttu-id="18ff4-593">19</span><span class="sxs-lookup"><span data-stu-id="18ff4-593">19</span></span>                   |
| <span data-ttu-id="18ff4-594">186</span><span class="sxs-lookup"><span data-stu-id="18ff4-594">186</span></span>                | <span data-ttu-id="18ff4-595">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-595">7</span></span>                    |
| <span data-ttu-id="18ff4-596">193</span><span class="sxs-lookup"><span data-stu-id="18ff4-596">193</span></span>                | <span data-ttu-id="18ff4-597">7</span><span class="sxs-lookup"><span data-stu-id="18ff4-597">7</span></span>                    |
