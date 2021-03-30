---
title: Umsatzsteuererklärung für Deutschland
description: Dieses Thema enthält Informationen zum Generieren von QR-Rechnungen und zum Verarbeiten eingehender QR-Rechnungen.
author: anasyash
manager: AnnBe
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Germany
ms.author: v-lenest
ms.search.validFrom: 2019-06-01
ms.dyn365.ops.version: 10.0.0
ms.openlocfilehash: 3f36ad1d0c674a6d96037dd406cd0d3fea6868f0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5246858"
---
# <a name="vat-declaration-for-germany"></a><span data-ttu-id="20955-103">Umsatzsteuererklärung für Deutschland</span><span class="sxs-lookup"><span data-stu-id="20955-103">VAT declaration for Germany</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="20955-104">In diesem Thema wird erläutert, wie Sie die Mehrwertsteuererklärung für juristische Personen in Deutschland einrichten und erstellen.</span><span class="sxs-lookup"><span data-stu-id="20955-104">This topic explains how to set up and generate the value-added tax (VAT) declaration for legal entities in Germany.</span></span>

<span data-ttu-id="20955-105">Weitere Informationen zur Einrichtung der Mehrwertsteuererklärung finden Sie unter [MwSt-Berichterstattung für Europa](emea-vat-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="20955-105">For general information about how to set up the VAT statement, see [VAT reporting for Europe](emea-vat-reporting.md).</span></span>

## <a name="set-up-sales-tax-reporting-codes-for-vat-reporting"></a><span data-ttu-id="20955-106">Mehrwertsteuer-Codes für Mehrwertsteuererklärung einrichten</span><span class="sxs-lookup"><span data-stu-id="20955-106">Set up sales tax reporting codes for VAT reporting</span></span>

<span data-ttu-id="20955-107">Richten Sie die Codes für die Mehrwertsteuererklärung ein, indem Sie die Anweisungen in [Mehrwertsteuer-Erklärungscodes einrichten](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="20955-107">Set up sales tax reporting codes by following the instructions in [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).</span></span> <span data-ttu-id="20955-108">Die folgende Tabelle enthält ein Beispiel für Umsatzsteuer-Berichtscodes für Deutschland.</span><span class="sxs-lookup"><span data-stu-id="20955-108">The following table provides an example of sales tax reporting codes for Germany.</span></span>

<table width="614">
<thead>
<tr>
<td width="75">
<p><span data-ttu-id="20955-109"><strong>Code</strong></span><span class="sxs-lookup"><span data-stu-id="20955-109"><strong>Code</strong></span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-110"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="20955-110"><strong>Description</strong></span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-111"><strong>Element in der XML-Datei der Umsatzsteuererklärung</strong></span><span class="sxs-lookup"><span data-stu-id="20955-111"><strong>Element in the XML file of the VAT declaration</strong></span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-112"><strong>Steuerbemessungsgrundlage oder Steuerbetrag</strong></span><span class="sxs-lookup"><span data-stu-id="20955-112"><strong>Tax base or tax amount</strong></span></span></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="20955-113"><strong>Steuerfreier Verkauf mit Vorsteuerabzug für innergemeinschaftliche Lieferungen (&sect;4, Nr. 1b des UStG [Umsatzsteuergesetz</strong><strong> oder </strong><strong>Mehrwertsteuergesetz])</strong></span><span class="sxs-lookup"><span data-stu-id="20955-113"><strong>Tax-free sales with input tax deduction for intra-community supplies (&sect;4, no. 1, letter b of the UStG [Umsatzsteuergesetz</strong><strong>, or </strong><strong>VAT law])</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-114">41</span><span class="sxs-lookup"><span data-stu-id="20955-114">41</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-115">Innergemeinschaftlicher Versand (&sect;4, Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-115">Intra-community shipment (&sect;4, no.</span></span> <span data-ttu-id="20955-116">1b des UStG) für Kunden mit Steuerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="20955-116">1b of the UStG) to customers with tax registration.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-117">Kz41</span><span class="sxs-lookup"><span data-stu-id="20955-117">Kz41</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-118">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-118">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-119">44</span><span class="sxs-lookup"><span data-stu-id="20955-119">44</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-120">Innergemeinschaftliche Lieferungen von Neufahrzeugen an Kunden ohne Umsatzsteuer-Identifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="20955-120">Intra-community deliveries of new vehicles to customers without a VAT ID.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-121">Kz44</span><span class="sxs-lookup"><span data-stu-id="20955-121">Kz44</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-122">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-122">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-123">49</span><span class="sxs-lookup"><span data-stu-id="20955-123">49</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-124">Innergemeinschaftliche Lieferungen von Neufahrzeugen außerhalb eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="20955-124">Intra-community deliveries of new vehicles outside a company.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-125">Kz49</span><span class="sxs-lookup"><span data-stu-id="20955-125">Kz49</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-126">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-126">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-127">43</span><span class="sxs-lookup"><span data-stu-id="20955-127">43</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-128">Zusätzliche steuerfreie Verkäufe mit Vorsteuerabzug (z. B. Exporte).</span><span class="sxs-lookup"><span data-stu-id="20955-128">Additional tax-free sales with input tax deduction (for example, exports).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-129">Kz43</span><span class="sxs-lookup"><span data-stu-id="20955-129">Kz43</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-130">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-130">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="20955-131"><strong>Steuerfreie Verkäufe ohne Vorsteuerabzug (z. B. Verkäufe nach &sect;4, Nr. 8 bis 28 des UStG)</strong></span><span class="sxs-lookup"><span data-stu-id="20955-131"><strong>Tax-free sales without input tax deduction (for example, sales according to &sect;4, no. 8 through 28 of the UStG)</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-132">48</span><span class="sxs-lookup"><span data-stu-id="20955-132">48</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-133">Steuerfreier Verkauf ohne Vorsteuerabzug.</span><span class="sxs-lookup"><span data-stu-id="20955-133">Tax-free sales without input tax deduction.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-134">Kz48</span><span class="sxs-lookup"><span data-stu-id="20955-134">Kz48</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-135">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-135">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="20955-136"><strong>Steuerpflichtiger Umsatz</strong></span><span class="sxs-lookup"><span data-stu-id="20955-136"><strong>Taxable sales</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-137">81</span><span class="sxs-lookup"><span data-stu-id="20955-137">81</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-138">Steuerbemessungsgrundlage für Lieferungen oder Leistungen, die mit 19 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="20955-138">Tax base for deliveries or services that are charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-139">Kz81</span><span class="sxs-lookup"><span data-stu-id="20955-139">Kz81</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-140">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-140">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-141">181</span><span class="sxs-lookup"><span data-stu-id="20955-141">181</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-142">Steuerbetrag für Lieferungen oder Leistungen, die mit 19 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="20955-142">Tax amount for deliveries or services that are charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-143">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="20955-143">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-144">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-144">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-145">86</span><span class="sxs-lookup"><span data-stu-id="20955-145">86</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-146">Steuerbemessungsgrundlage für Lieferungen oder Leistungen, die mit 7 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="20955-146">Tax base for deliveries or services that are charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-147">Kz86</span><span class="sxs-lookup"><span data-stu-id="20955-147">Kz86</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-148">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-148">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-149">186</span><span class="sxs-lookup"><span data-stu-id="20955-149">186</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-150">Steuerbetrag für Lieferungen oder Leistungen, die mit 7 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="20955-150">Tax amount for deliveries or services that are charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-151">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="20955-151">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-152">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-152">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-153">35</span><span class="sxs-lookup"><span data-stu-id="20955-153">35</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-154">Steuerbemessungsgrundlage für Lieferungen oder Leistungen zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="20955-154">Tax base for deliveries or services at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-155">Kz35</span><span class="sxs-lookup"><span data-stu-id="20955-155">Kz35</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-156">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-156">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-157">36</span><span class="sxs-lookup"><span data-stu-id="20955-157">36</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-158">Steuerbetrag für Lieferungen oder Leistungen zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="20955-158">Tax amount for deliveries or services at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-159">Kz36</span><span class="sxs-lookup"><span data-stu-id="20955-159">Kz36</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-160">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-160">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-161">77</span><span class="sxs-lookup"><span data-stu-id="20955-161">77</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-162">Lieferungen von land- und forstwirtschaftlichen Betrieben nach &sect;24 des UStG an Kunden mit einer Umsatzsteuer-Identifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="20955-162">Deliveries of agricultural and forestry businesses, according to &sect;24 of the UStG, to customers who have a VAT ID.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-163">Kz77</span><span class="sxs-lookup"><span data-stu-id="20955-163">Kz77</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-164">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-164">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-165">76</span><span class="sxs-lookup"><span data-stu-id="20955-165">76</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-166">Steuerbemessungsgrundlage des Umsatzes, für den die Steuer zu zahlen ist &sect;24 des UStG (Sägewerksprodukte, Getränke und alkoholische Getränke wie Wein).</span><span class="sxs-lookup"><span data-stu-id="20955-166">Tax base of turnover that tax is payable for, according to &sect;24 of the UStG (sawmill products, beverages and alcoholic liquids, such as wine).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-167">Kz76</span><span class="sxs-lookup"><span data-stu-id="20955-167">Kz76</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-168">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-168">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-169">80</span><span class="sxs-lookup"><span data-stu-id="20955-169">80</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-170">Steuerbetrag des Umsatzes, für den die Steuer zu zahlen ist &sect;24 des UStG (Sägewerksprodukte, Getränke und alkoholische Getränke wie Wein).</span><span class="sxs-lookup"><span data-stu-id="20955-170">Tax amount of turnover that tax is payable for, according to &sect;24 of the UStG (sawmill products, beverages and alcoholic liquids, such as wine).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-171">Kz80</span><span class="sxs-lookup"><span data-stu-id="20955-171">Kz80</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-172">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-172">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="20955-173"><strong>Innergemeinschaftliche Akquisitionen und Mehrwertsteuer für solche Akquisitionen</strong></span><span class="sxs-lookup"><span data-stu-id="20955-173"><strong>Intra-community acquisitions and VAT payable for such acquisitions</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-174">91</span><span class="sxs-lookup"><span data-stu-id="20955-174">91</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-175">Steuerfreie innergemeinschaftliche Akquisitionen.</span><span class="sxs-lookup"><span data-stu-id="20955-175">Tax-free intra-community acquisitions.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-176">Kz91</span><span class="sxs-lookup"><span data-stu-id="20955-176">Kz91</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-177">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-177">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-178">89</span><span class="sxs-lookup"><span data-stu-id="20955-178">89</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-179">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="20955-179">Tax base for the acquisition of goods from countries in the European Union (EU), charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-180">Kz89</span><span class="sxs-lookup"><span data-stu-id="20955-180">Kz89</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-181">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-181">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-182">189</span><span class="sxs-lookup"><span data-stu-id="20955-182">189</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-183">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="20955-183">Tax amount for the acquisition of goods from countries in the EU, charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-184">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="20955-184">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-185">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-185">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-186">93</span><span class="sxs-lookup"><span data-stu-id="20955-186">93</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-187">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="20955-187">Tax base for the acquisition of goods from countries in the EU, charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-188">Kz93</span><span class="sxs-lookup"><span data-stu-id="20955-188">Kz93</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-189">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-189">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-190">193</span><span class="sxs-lookup"><span data-stu-id="20955-190">193</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-191">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="20955-191">Tax amount for the acquisition of goods from countries in the EU, charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-192">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="20955-192">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-193">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-193">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-194">95</span><span class="sxs-lookup"><span data-stu-id="20955-194">95</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-195">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="20955-195">Tax base for the acquisition of goods from countries in the EU at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-196">Kz95</span><span class="sxs-lookup"><span data-stu-id="20955-196">Kz95</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-197">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-197">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-198">98</span><span class="sxs-lookup"><span data-stu-id="20955-198">98</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-199">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="20955-199">Tax amount for the acquisition of goods from countries in the EU at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-200">Kz98</span><span class="sxs-lookup"><span data-stu-id="20955-200">Kz98</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-201">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-201">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-202">94</span><span class="sxs-lookup"><span data-stu-id="20955-202">94</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-203">Steuerbemessungsgrundlage für innergemeinschaftliche Anschaffungen neuer Fahrzeuge (&sect;1b, Absätze 2 und 3 des UStG) von Lieferanten ohne MwSt.-ID zum allgemeinen Steuersatz.</span><span class="sxs-lookup"><span data-stu-id="20955-203">Tax base for intra-community acquisitions of new vehicles (&sect;1b, paragraphs 2 and 3 of the UStG) from suppliers without a VAT ID, at the general tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-204">Kz94</span><span class="sxs-lookup"><span data-stu-id="20955-204">Kz94</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-205">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-205">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-206">96</span><span class="sxs-lookup"><span data-stu-id="20955-206">96</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-207">Steuerbetrag für innergemeinschaftliche Anschaffungen neuer Fahrzeuge (&sect;1b, Absätze 2 und 3 des UStG) von Lieferanten ohne MwSt.-ID zum allgemeinen Steuersatz.</span><span class="sxs-lookup"><span data-stu-id="20955-207">Tax amount for intra-community acquisitions of new vehicles (&sect;1b, paragraphs 2 and 3 of the UStG) from suppliers without a VAT ID, at the general tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-208">Kz96</span><span class="sxs-lookup"><span data-stu-id="20955-208">Kz96</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-209">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-209">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="20955-210"><strong>Zusätzliche Informationen zum Vertrieb</strong></span><span class="sxs-lookup"><span data-stu-id="20955-210"><strong>Additional information about sales</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-211">42</span><span class="sxs-lookup"><span data-stu-id="20955-211">42</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-212">Lieferungen des ersten Kunden für gemeinschaftsinterne Dreieckstransaktionen (&sect;25b des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-212">Deliveries by the first customer for intra-community triangular transactions (&sect;25b of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-213">Kz42</span><span class="sxs-lookup"><span data-stu-id="20955-213">Kz42</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-214">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-214">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-215">60</span><span class="sxs-lookup"><span data-stu-id="20955-215">60</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-216">Steuerpflichtiger Umsatz des ausführenden Unternehmers, für den der Leistungsempfänger die Steuer schuldet, gemäß &sect;13b (5) des UStG.</span><span class="sxs-lookup"><span data-stu-id="20955-216">Taxable sales of the performing entrepreneur that the service recipient owes the tax for, according to &sect;13b (5) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-217">Kz60</span><span class="sxs-lookup"><span data-stu-id="20955-217">Kz60</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-218">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-218">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-219">21</span><span class="sxs-lookup"><span data-stu-id="20955-219">21</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-220">Sonstige nicht steuerpflichtige Dienstleistungen gemäß &sect;18b, Satz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-220">Other non-taxable services according to &sect;18b, sentence 1, no.</span></span> <span data-ttu-id="20955-221">2 des UStG.</span><span class="sxs-lookup"><span data-stu-id="20955-221">2 of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-222">Kz21</span><span class="sxs-lookup"><span data-stu-id="20955-222">Kz21</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-223">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-223">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-224">45</span><span class="sxs-lookup"><span data-stu-id="20955-224">45</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-225">Sonstige nicht steuerpflichtige Verkäufe (wenn der Erfüllungsort nicht in Deutschland liegt).</span><span class="sxs-lookup"><span data-stu-id="20955-225">Other non-taxable sales (where the place of performance isn't in Germany).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-226">Kz45</span><span class="sxs-lookup"><span data-stu-id="20955-226">Kz45</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-227">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-227">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="20955-228"><strong>Begünstigter als Steuerschuldner (&sect;13b des UStG)</strong></span><span class="sxs-lookup"><span data-stu-id="20955-228"><strong>Beneficiary as tax debtor (&sect;13b of the UStG)</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-229">46</span><span class="sxs-lookup"><span data-stu-id="20955-229">46</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-230">Steuerbemessungsgrundlage für sonstige Leistungen gemäß &sect;3A (2) UStG eines Unternehmers, der sich im Rest der Gemeinde befindet (&sect;13b (1) des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-230">Tax base for other services in accordance with &sect;3a (2) UStG of an entrepreneur that is located in the rest of the community (&sect;13b (1) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-231">Kz46</span><span class="sxs-lookup"><span data-stu-id="20955-231">Kz46</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-232">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-232">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-233">47</span><span class="sxs-lookup"><span data-stu-id="20955-233">47</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-234">Steuerbetrag für sonstige Leistungen gemäß &sect;3A (2) UStG eines Unternehmers, der sich im Rest der Gemeinde befindet (&sect;13b (1) des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-234">Tax amount for other services in accordance with &sect;3a (2) UStG of an entrepreneur that is located in the rest of the community (&sect;13b (1) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-235">Kz47</span><span class="sxs-lookup"><span data-stu-id="20955-235">Kz47</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-236">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-236">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-237">73</span><span class="sxs-lookup"><span data-stu-id="20955-237">73</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-238">Steuerbemessungsgrundlage des Umsatzes, der unter das Grundsteuergesetz fällt &ndash; insbesondere Lieferungen von Grundstücken, für die sich der ausführende Unternehmer für eine Steuerschuld gemäß &sect;9 (3) des UStG entschieden hat.</span><span class="sxs-lookup"><span data-stu-id="20955-238">Tax base of turnover that is covered by the property transfer tax law &ndash; in particular, deliveries of land for which the performing entrepreneur has opted for tax liability in accordance with &sect;9 (3) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-239">Kz73</span><span class="sxs-lookup"><span data-stu-id="20955-239">Kz73</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-240">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-240">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-241">74</span><span class="sxs-lookup"><span data-stu-id="20955-241">74</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-242">Steuerbetrag des Umsatzes, der unter das Grundsteuergesetz fällt &ndash; insbesondere Lieferungen von Grundstücken, für die sich der ausführende Unternehmer für eine Steuerschuld gemäß &sect;9 (3) des UStG entschieden hat.</span><span class="sxs-lookup"><span data-stu-id="20955-242">Tax amount of turnover that is covered by the property transfer tax law &ndash; in particular, deliveries of land for which the performing entrepreneur has opted for tax liability in accordance with &sect;9 (3) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-243">Kz74</span><span class="sxs-lookup"><span data-stu-id="20955-243">Kz74</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-244">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-244">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-245">84</span><span class="sxs-lookup"><span data-stu-id="20955-245">84</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-246">Steuerbemessungsgrundlage für andere Dienstleistungen (&sect;13b (2), Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-246">Tax base of other services (&sect;13b (2), no.</span></span> <span data-ttu-id="20955-247">1, 2 und 4 bis 11 des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-247">1, 2, and 4 through 11 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-248">Kz84</span><span class="sxs-lookup"><span data-stu-id="20955-248">Kz84</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-249">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="20955-249">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-250">85</span><span class="sxs-lookup"><span data-stu-id="20955-250">85</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-251">Steuerbetrag für andere Dienstleistungen (&sect;13b (2), Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-251">Tax amount of other services (&sect;13b (2), no.</span></span> <span data-ttu-id="20955-252">1, 2 und 4 bis 11 des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-252">1, 2, and 4 through 11 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-253">Kz85</span><span class="sxs-lookup"><span data-stu-id="20955-253">Kz85</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-254">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-254">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="20955-255"><strong>Abzugsfähige Vorsteuerbeträge</strong></span><span class="sxs-lookup"><span data-stu-id="20955-255"><strong>Deductible input tax amounts</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-256">66</span><span class="sxs-lookup"><span data-stu-id="20955-256">66</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-257">Steuer auf Eingaben aus Rechnungen anderer Unternehmen (&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-257">Tax on input from invoices of other companies (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="20955-258">1 des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-258">1 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-259">Kz66</span><span class="sxs-lookup"><span data-stu-id="20955-259">Kz66</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-260">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-260">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-261">61</span><span class="sxs-lookup"><span data-stu-id="20955-261">61</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-262">Vorsteuerbetrag aus innergemeinschaftlichen Erwerb von Gegenständen (&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-262">Input VAT amount from intra-community acquisitions of objects (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="20955-263">3 des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-263">3 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-264">Kz61</span><span class="sxs-lookup"><span data-stu-id="20955-264">Kz61</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-265">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-265">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-266">62</span><span class="sxs-lookup"><span data-stu-id="20955-266">62</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-267">Anfallender Umsatzsteuerimport(&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-267">Import sales tax that is incurred (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="20955-268">2 des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-268">2 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-269">Kz62</span><span class="sxs-lookup"><span data-stu-id="20955-269">Kz62</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-270">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-270">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-271">67</span><span class="sxs-lookup"><span data-stu-id="20955-271">67</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-272">Vorsteuerbeträge aus Dienstleistungen im Sinne von &sect;13b des UStG (&sect;15, Absatz 1, Klausel 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-272">Input tax amounts from services within the meaning of &sect;13b of the UStG (&sect;15, paragraph 1, clause 1, no.</span></span> <span data-ttu-id="20955-273">4 des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-273">4 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-274">Kz67</span><span class="sxs-lookup"><span data-stu-id="20955-274">Kz67</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-275">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-275">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-276">63</span><span class="sxs-lookup"><span data-stu-id="20955-276">63</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-277">Vorsteuerbeträge, die nach allgemeinen Durchschnittssätzen berechnet werden (&sect;23 und &sect;23A des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-277">Input tax amounts that are calculated according to general average rates (&sect;23 and &sect;23a of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-278">Kz63</span><span class="sxs-lookup"><span data-stu-id="20955-278">Kz63</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-279">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-279">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-280">64</span><span class="sxs-lookup"><span data-stu-id="20955-280">64</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-281">Korrektur des Vorsteuerabzugs (&sect;15A des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-281">Correction of input tax deduction (&sect;15a of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-282">Kz64</span><span class="sxs-lookup"><span data-stu-id="20955-282">Kz64</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-283">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-283">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-284">59</span><span class="sxs-lookup"><span data-stu-id="20955-284">59</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-285">Vorsteuerabzug für innergemeinschaftliche Lieferungen neuer Fahrzeuge außerhalb eines Unternehmens (&sect;2A des UStG) und Kleinunternehmen im Sinne von &sect;19 (1) des UStG (&sect;15 (4A) des UStG).</span><span class="sxs-lookup"><span data-stu-id="20955-285">Input tax deduction for intra-community deliveries of new vehicles outside a company (&sect;2a of the UStG) and small businesses within the meaning of &sect;19 (1) of the UStG (&sect;15 (4a) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-286">Kz59</span><span class="sxs-lookup"><span data-stu-id="20955-286">Kz59</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-287">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-287">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="20955-288"><strong>Sonstige Steuerbeträge</strong></span><span class="sxs-lookup"><span data-stu-id="20955-288"><strong>Other tax amounts</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-289">65</span><span class="sxs-lookup"><span data-stu-id="20955-289">65</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-290">Steuern aufgrund von Änderungen in der Form der Besteuerung und Nachsteuer auf besteuerte Anzahlungen usw. aufgrund von Änderungen des Steuersatzes.</span><span class="sxs-lookup"><span data-stu-id="20955-290">Tax because of changes in the form of taxation, and after-tax on taxed down payments, and so on, because of changes in tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-291">Kz65</span><span class="sxs-lookup"><span data-stu-id="20955-291">Kz65</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-292">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-292">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-293">69</span><span class="sxs-lookup"><span data-stu-id="20955-293">69</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-294">Steuerbeträge, die auf Rechnungen falsch oder unplausibel ausgewiesen sind (&sect;14c des UStG) sowie Steuerbeträge, die in Übereinstimmung mit &sect;6A (4), Satz 2; &sect;17 (1), Satz 6 und &sect;25b (2) des UStG <strong>geschuldet</strong> sind oder <strong>geschuldete Steuerbeträge</strong> von einem Outsourcer oder Lagerhalter gemäß &sect;13A (2) 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="20955-294">Tax amounts that are shown incorrectly or unjustifiably on invoices (&sect;14c of the UStG), and also tax amounts that are <strong>owed</strong> in accordance with &sect;6a (4), sentence 2; &sect;17 (1), sentence 6; and &sect;25b (2) of the UStG, or <strong>tax amounts that are owed</strong> by an outsourcer or warehouse keeper in accordance with &sect;13a (2) 1, no.</span></span> <span data-ttu-id="20955-295">6 des UStG.</span><span class="sxs-lookup"><span data-stu-id="20955-295">6 of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-296">Kz69</span><span class="sxs-lookup"><span data-stu-id="20955-296">Kz69</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-297">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-297">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-298">39</span><span class="sxs-lookup"><span data-stu-id="20955-298">39</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-299">Abzug der vereinbarten Sondervorauszahlung für eine langfristige Verlängerung (die in der Regel erst in der letzten Vorankündigung des Steuerzeitraums erfolgt).</span><span class="sxs-lookup"><span data-stu-id="20955-299">Deduction of the stipulated special advance payment for long-term extension (which usually will be completed only in the last advance notification of the taxation period).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-300">Kz39</span><span class="sxs-lookup"><span data-stu-id="20955-300">Kz39</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-301">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-301">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="20955-302">83</span><span class="sxs-lookup"><span data-stu-id="20955-302">83</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="20955-303">Gesamtbetrag der Mehrwertsteuer (Mehrwertsteuer-Vorauszahlung oder Mehrwertsteuerüberschuss).</span><span class="sxs-lookup"><span data-stu-id="20955-303">Total VAT amount (VAT advance payment or VAT surplus).</span></span></p>
<p><span data-ttu-id="20955-304">Bei der Umsatzsteuererklärung im XML-Format wird der Wert in diesem Feld automatisch als Summe der Berichtscodes 181, 186, 36, 80, 189, 193, 98, 96, 47, 74 und 85 abzüglich der Berichtscodes 66, 61, 62, 67, 63, 64, 59, 69 und 39 berechnet.</span><span class="sxs-lookup"><span data-stu-id="20955-304">On the VAT declaration in XML format, the value in this box is automatically calculated as the sum of reporting codes 181, 186, 36, 80, 189, 193, 98, 96, 47, 74, and 85, minus reporting codes 66, 61, 62, 67, 63, 64, 59, 69, and 39.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="20955-305">Kz83</span><span class="sxs-lookup"><span data-stu-id="20955-305">Kz83</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="20955-306">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="20955-306">Tax amount</span></span></p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>

> [!NOTE]
> <span data-ttu-id="20955-307">Beispiele für Formen von Mehrwertsteuererklärungen, die Deklarationszeilencodes enthalten, finden Sie unter [Formulare im Mehrwertsteuerverfahren für das Jahr 2020](https://umsatzsteuer-voranmeldung-2020.taxpool.net/Umsatzsteuer-Voranmeldung-2020.pdf).</span><span class="sxs-lookup"><span data-stu-id="20955-307">For sample forms of advance VAT returns that include declaration row codes, see [Forms in the VAT procedure for the year 2020](https://umsatzsteuer-voranmeldung-2020.taxpool.net/Umsatzsteuer-Voranmeldung-2020.pdf).</span></span>

## <a name="prerequisite"></a><span data-ttu-id="20955-308">Voraussetzung</span><span class="sxs-lookup"><span data-stu-id="20955-308">Prerequisite</span></span>

<span data-ttu-id="20955-309">Bevor Sie beginnen, rufen Sie die Seite **Hauptbuchparameter** auf, und erweitern Sie das Inforegister **Steueroptionen**.</span><span class="sxs-lookup"><span data-stu-id="20955-309">Before you begin, go to the **General ledger parameters** page and expand the **Tax options** FastTab.</span></span> <span data-ttu-id="20955-310">Vergewissern Sie sich, dass in der Feldgruppe **Sonderbericht** der Parameter **Korrekturen einbeziehen** nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="20955-310">In the **Special report** field group, make sure that the **Include corrections** parameter isn't enabled.</span></span> 

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="20955-311">Mehrwertsteuercodes einrichten</span><span class="sxs-lookup"><span data-stu-id="20955-311">Set up sales tax codes</span></span>

<span data-ttu-id="20955-312">Richten Sie die Codes für die Mehrwertsteuererklärung ein, indem Sie die Anweisungen in [Mehrwertsteuercodes für MwSt-Berichterstattung](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) und [Mehrwertsteuerübersicht](../general-ledger/indirect-taxes-overview.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="20955-312">Set up sales tax codes by following the instructions in [Sales tax codes for VAT reporting](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) and [Sales tax overview](../general-ledger/indirect-taxes-overview.md).</span></span>

> [!NOTE]
> <span data-ttu-id="20955-313">In einer deutschen juristischen Entität sollten Umsatzsteuerkennzeichen für steuerfreie Verkäufe nach folgenden Regeln eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="20955-313">In a German legal entity, sales tax codes for tax-free sales should be set up according to the following rules:</span></span>
>
> - <span data-ttu-id="20955-314">Der Steuersatz beträgt mehr als 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="20955-314">The tax rate is more than 0 (zero).</span></span>
> - <span data-ttu-id="20955-315">Das Steuerkennzeichen ist als **Befreit** auf der **Umsatzsteuergruppen**-Seite gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="20955-315">The tax code is marked as **Exempt** on the **Sales tax groups** page.</span></span>

## <a name="create-a-vat-declaration-in-xml-format"></a><a name= "createvatdecxmlformat"></a><span data-ttu-id="20955-316">Erstellen einer Umsatzsteuererklärung im XML-Format</span><span class="sxs-lookup"><span data-stu-id="20955-316">Create a VAT declaration in XML format</span></span>

1. <span data-ttu-id="20955-317">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in der **Bibliothek der freigegebenen Anlagen** laden Sie die neuesten Versionen der Konfigurationen für die elektronische Berichterstattung (ER) für das Format der Umsatzsteuererklärung herunter:</span><span class="sxs-lookup"><span data-stu-id="20955-317">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in the **Shared asset library**, download the latest versions of the Electronic reporting (ER) configurations for the VAT declaration format:</span></span>

    - <span data-ttu-id="20955-318">**Elster (DE)**</span><span class="sxs-lookup"><span data-stu-id="20955-318">**Elster (DE)**</span></span>

    <span data-ttu-id="20955-319">Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="20955-319">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

2. <span data-ttu-id="20955-320">Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer-Erklärungscodes**.</span><span class="sxs-lookup"><span data-stu-id="20955-320">Go to **Tax** \> **Setup** \> **Sales tax** \> **Electronic tax declaration setup**.</span></span>
3. <span data-ttu-id="20955-321">Im Feld **Formatzuordnung** wählen Sie das Format **Elster (DE)** aus, das Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="20955-321">In the **Format mapping** field, select the **Elster (DE)** format that you downloaded earlier.</span></span>
4. <span data-ttu-id="20955-322">Wechseln Sie zu **Steuer \> Erklärungen \> Mehrwertsteuer \> Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="20955-322">Go to **Tax \> Declarations \> Sales tax \> Report sales tax for settlement period**.</span></span>
5. <span data-ttu-id="20955-323">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="20955-323">In the **Report sales tax for settlement period** dialog box, set the following fields.</span></span>

| <span data-ttu-id="20955-324">**Feld**</span><span class="sxs-lookup"><span data-stu-id="20955-324">**Field**</span></span>                 | <span data-ttu-id="20955-325">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20955-325">**Description**</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20955-326">Ausgleichsperiode</span><span class="sxs-lookup"><span data-stu-id="20955-326">Settlement period</span></span>         | <span data-ttu-id="20955-327">Wählen Sie den gewünschten Berichtszeitraum aus.</span><span class="sxs-lookup"><span data-stu-id="20955-327">Select the applicable reporting period.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="20955-328">Startdatum</span><span class="sxs-lookup"><span data-stu-id="20955-328">From date</span></span>                 | <span data-ttu-id="20955-329">Geben Sie das erste Datum des zu berechnenden Mehrwertsteuer-Abrechnungszeitraums an, um die Mehrwertsteuer zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="20955-329">Enter the first date of the sales tax settlement period that sales tax should be calculated for.</span></span> <span data-ttu-id="20955-330">Dieser Wert entspricht dem Datum im Feld **Vom** auf der **Mehrwertsteuer-Abrechnungszeitraum**-Seite.</span><span class="sxs-lookup"><span data-stu-id="20955-330">This value corresponds to the date in the **From** field on the **Sales tax settlement periods** page.</span></span>                                                                                 |
| <span data-ttu-id="20955-331">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="20955-331">Transaction date</span></span>          | <span data-ttu-id="20955-332">Geben Sie das Datum an, für das die Mehrwertsteuererklärung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="20955-332">Enter the date when the sales tax report is calculated.</span></span> <span data-ttu-id="20955-333">Der aktuelle Wert ist das aktuelle Datum.</span><span class="sxs-lookup"><span data-stu-id="20955-333">The default value is the current date.</span></span> <span data-ttu-id="20955-334">Die Mehrwertsteuerzahlung wird für alle Buchungen berechnet, die im Abrechnungszeitraum gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="20955-334">The sales tax payment is calculated for all transactions that were posted during the settlement period.</span></span>                                                                                  |
| <span data-ttu-id="20955-335">Mehrwertsteuer, Zahlungsversion</span><span class="sxs-lookup"><span data-stu-id="20955-335">Sales tax payment version</span></span> | <span data-ttu-id="20955-336">Wählen Sie den Mehrwertsteuer-Ausgleichstyp.</span><span class="sxs-lookup"><span data-stu-id="20955-336">Select the type of sales tax settlement.</span></span> <span data-ttu-id="20955-337">Wenn diese Umsatzsteuerabrechnung die erste Umsatzsteuerabrechnung für den Zeitraum ist, wählen Sie **Original**.</span><span class="sxs-lookup"><span data-stu-id="20955-337">If this sales tax settlement is the first sales tax settlement for the period, select **Original**.</span></span> <span data-ttu-id="20955-338">Wenn bereits eine Umsatzsteuerabrechnung generiert wurde, wählen Sie **Neueste Korrekturen**.</span><span class="sxs-lookup"><span data-stu-id="20955-338">If a sales tax settlement has already been generated, select **Latest corrections**.</span></span> <span data-ttu-id="20955-339">Weitere Informationen finden Sie unter [Eine Mehrwertsteuerzahlung erstellen](../general-ledger/tasks/create-sales-tax-payment.md).</span><span class="sxs-lookup"><span data-stu-id="20955-339">For more information, see [Create a sales tax payment](../general-ledger/tasks/create-sales-tax-payment.md).</span></span> |

6. <span data-ttu-id="20955-340">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-340">Select **OK**.</span></span>
7. <span data-ttu-id="20955-341">Im Dialogfeld **Deutsche Mehrwertsteuererklärung** stellen Sie die folgenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="20955-341">In the **German sales tax report** dialog box, set the following fields.</span></span>

| <span data-ttu-id="20955-342">**Feld**</span><span class="sxs-lookup"><span data-stu-id="20955-342">**Field**</span></span>                      | <span data-ttu-id="20955-343">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20955-343">**Description**</span></span>                                                                                                                                                 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20955-344">Elektronisches Steuerdokument erstellen</span><span class="sxs-lookup"><span data-stu-id="20955-344">Create electronic tax document</span></span> | <span data-ttu-id="20955-345">Setzen Sie diese Option auf **Ja**, um ein elektronisches Dokument zu erstellen, das die Details des Berichts enthält.</span><span class="sxs-lookup"><span data-stu-id="20955-345">Set this option to **Yes** to create an electronic document that contains the details of the report.</span></span>                                                            |
| <span data-ttu-id="20955-346">Separat übermittelte Dokumente</span><span class="sxs-lookup"><span data-stu-id="20955-346">Documents submitted separately</span></span> | <span data-ttu-id="20955-347">Setzen Sie diese Option auf **Ja**, wenn der gedruckte Bericht nicht zusammen mit dem elektronischen Dokument eingereicht wird.</span><span class="sxs-lookup"><span data-stu-id="20955-347">Set this option to **Yes** if the printed report isn't submitted together with the electronic document.</span></span> <span data-ttu-id="20955-348">In der XML-Datei sollte der Code Kz22 den Wert **1** haben.</span><span class="sxs-lookup"><span data-stu-id="20955-348">In the XML file, code Kz22 should have the value **1**.</span></span> |

8. <span data-ttu-id="20955-349">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-349">Select **OK**.</span></span> <span data-ttu-id="20955-350">Auf der **Elektronisches Steuererklärungsprotokoll**-Seite (**Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**) wird eine neue Zeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="20955-350">A new line is created on the **Electronic tax declaration log** page (**Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**).</span></span>

![Seite „Protokoll der elektronischen Steuererklärung“](media/1_Electronic_tax_declaration_log.png)

## <a name="preview-the-xml-file"></a><span data-ttu-id="20955-352">Vorschau der XML-Datei</span><span class="sxs-lookup"><span data-stu-id="20955-352">Preview the XML file</span></span>

1. <span data-ttu-id="20955-353">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**.</span><span class="sxs-lookup"><span data-stu-id="20955-353">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**.</span></span>
2. <span data-ttu-id="20955-354">Auf der Seite **Protokoll der elektronischen Steuererklärung**, wählen Sie die **Vorschau**-Registerkarte, um eine Vorschau der gemeldeten Werte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="20955-354">On the **Electronic tax declaration log** page, select the **Preview** tab to preview the reported values.</span></span>
3. <span data-ttu-id="20955-355">Um die XML-Datei zur weiteren Übermittlung (außerhalb des Systems) zu überprüfen oder zu speichern, wählen Sie die Zeile auf der **Protokoll der elektronischen Steuererklärung**-Seite, und wählen Sie dann das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="20955-355">To review or save the XML file for further submission (outside of the system), select the line on the **Electronic tax declaration log** page, and then select the paper clip symbol in the upper-right corner.</span></span>
4. <span data-ttu-id="20955-356">Die **Handhabung von Dokumenten**-Seite erscheint und zeigt die generierte Datei.</span><span class="sxs-lookup"><span data-stu-id="20955-356">The **Document handling** page appears and shows the generated file.</span></span> <span data-ttu-id="20955-357">Wählen Sie **Öffnen** oben auf der Seite, um die Datei in der Anwendung zu öffnen, die der XML-Erweiterung in Ihrem System zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="20955-357">Select **Open** at the top of the page to open the file in the application that is associated with the .xml extension in your system.</span></span>

## <a name="submission-the-vat-declaration-to-elster"></a><span data-ttu-id="20955-358">Senden Sie die Umsatzsteuererklärung an ELSTER</span><span class="sxs-lookup"><span data-stu-id="20955-358">Submission the VAT declaration to ELSTER</span></span>

<span data-ttu-id="20955-359">ELSTER (Elektronische Steuererklärung) ist ein deutsches Online-Finanzamt, das vom Bundeszentralen Finanzamt für die Online-Einreichung von Steuererklärungen konzipiert wurde.</span><span class="sxs-lookup"><span data-stu-id="20955-359">ELSTER (Elektronische Steuererklärung, or electronic tax declaration) is a German online tax office system that was designed by the Federal Central Tax Office for online submission of tax declarations.</span></span>

<span data-ttu-id="20955-360">Im [Entwicklerbereich](https://www.elster.de/elsterweb/entwickler/infoseite/download_eric_28.) auf der ELSTER-Website finden Sie Beispiele, die zeigen, wie Entwickler mit ELSTER Rich Client (ERiC) interagieren können, um Mehrwertsteuererklärungen im XML-Dateiformat einzureichen.</span><span class="sxs-lookup"><span data-stu-id="20955-360">The [Developers area](https://www.elster.de/elsterweb/entwickler/infoseite/download_eric_28.) of the ELSTER website provides examples that show how developers can interact with ELSTER Rich Client (ERiC) for the submission of VAT declarations in XML file format.</span></span> <span data-ttu-id="20955-361">Beispiele werden für C++, C\# und Java bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="20955-361">Examples are provided for C++, C\#, and Java.</span></span> <span data-ttu-id="20955-362">Um auf diesen Bereich der Website zugreifen zu können, müssen Sie [als Entwickler registriert](https://www.elster.de/elsterweb/registrierung-entwickler) sein.</span><span class="sxs-lookup"><span data-stu-id="20955-362">To access this area of the website, you must be [registered as a developer](https://www.elster.de/elsterweb/registrierung-entwickler).</span></span> <span data-ttu-id="20955-363">Ein Beispiel könnte Ihnen helfen, Ihre eigene ausführbare Datei zu erstellen, mit der Sie XML-Dateien über ERiC senden können.</span><span class="sxs-lookup"><span data-stu-id="20955-363">An example might help you create your own executable file that you can use to submit XML files via ERiC.</span></span> <span data-ttu-id="20955-364">Um eine ausführbare Datei zum Senden von XML-Dateien an ELSTER zu verwenden, müssen Sie ERiC Dynamics Link Libraries (DLLs) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="20955-364">To use an executable file to submit XML files to ELSTER, you must download ERiC dynamics-link libraries (DLLs).</span></span>

<span data-ttu-id="20955-365">Weitere Informationen zu ERiC-Versionen finden Sie unter [ELSTER-Website](https://www.elster.de/elsterweb/entwickler/infoseite/eric).</span><span class="sxs-lookup"><span data-stu-id="20955-365">For more information about ERiC releases, see [ELSTER website](https://www.elster.de/elsterweb/entwickler/infoseite/eric).</span></span>

## <a name="example"></a><a name="example"></a> <span data-ttu-id="20955-366">Beispiel</span><span class="sxs-lookup"><span data-stu-id="20955-366">Example</span></span>

<span data-ttu-id="20955-367">Das folgende Beispiel zeigt, wie Sie Umsatzsteuerkennzeichen und Umsatzsteuerberichtscodes einrichten, Transaktionen buchen und die deutsche Umsatzsteuererklärung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="20955-367">The following example shows how you can set up sales tax codes and sales tax reporting codes, post transactions, and generate the German VAT declaration.</span></span>

1. <span data-ttu-id="20955-368">Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuercodes** und richten Sie die folgenden Umsatzsteuerkennzeichen ein.</span><span class="sxs-lookup"><span data-stu-id="20955-368">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**, and set up the following sales tax codes.</span></span>

| <span data-ttu-id="20955-369">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="20955-369">**Sales tax code**</span></span> | <span data-ttu-id="20955-370">**Prozentsatz**</span><span class="sxs-lookup"><span data-stu-id="20955-370">**Percentage**</span></span> | <span data-ttu-id="20955-371">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="20955-371">**Description**</span></span>                                                                       |
|--------------------|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="20955-372">VAT19</span><span class="sxs-lookup"><span data-stu-id="20955-372">VAT19</span></span>              | <span data-ttu-id="20955-373">19</span><span class="sxs-lookup"><span data-stu-id="20955-373">19</span></span>             | <span data-ttu-id="20955-374">Inlandsverkäufe mit einer Quote von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="20955-374">Domestic sales at a rate of 19 percent.</span></span>                                               |
| <span data-ttu-id="20955-375">VAT7</span><span class="sxs-lookup"><span data-stu-id="20955-375">VAT7</span></span>               | <span data-ttu-id="20955-376">7</span><span class="sxs-lookup"><span data-stu-id="20955-376">7</span></span>              | <span data-ttu-id="20955-377">Inlandsverkäufe mit einer Quote von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="20955-377">Domestic sales at a rate of 7 percent.</span></span>                                                |
| <span data-ttu-id="20955-378">InVAT19</span><span class="sxs-lookup"><span data-stu-id="20955-378">InVAT19</span></span>            | <span data-ttu-id="20955-379">19</span><span class="sxs-lookup"><span data-stu-id="20955-379">19</span></span>             | <span data-ttu-id="20955-380">Inlandseinkäufe mit einer Quote von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="20955-380">Domestic purchases at a rate of 19 percent.</span></span>                                           |
| <span data-ttu-id="20955-381">InVAT7</span><span class="sxs-lookup"><span data-stu-id="20955-381">InVAT7</span></span>             | <span data-ttu-id="20955-382">7</span><span class="sxs-lookup"><span data-stu-id="20955-382">7</span></span>              | <span data-ttu-id="20955-383">Inlandseinkäufe mit einer Quote von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="20955-383">Domestic purchases at a rate of 7 percent.</span></span>                                            |
| <span data-ttu-id="20955-384">EU19</span><span class="sxs-lookup"><span data-stu-id="20955-384">EU19</span></span>               | <span data-ttu-id="20955-385">19</span><span class="sxs-lookup"><span data-stu-id="20955-385">19</span></span>             | <span data-ttu-id="20955-386">EU-Einkäufe mit einer Quote von 19 Prozent, wobei die **Erwerbsteuer (USA)**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="20955-386">EU purchases at a rate of 19 percent, where the **Use tax** option is set to **Yes**.</span></span> |
| <span data-ttu-id="20955-387">EU7</span><span class="sxs-lookup"><span data-stu-id="20955-387">EU7</span></span>                | <span data-ttu-id="20955-388">7</span><span class="sxs-lookup"><span data-stu-id="20955-388">7</span></span>              | <span data-ttu-id="20955-389">EU-Einkäufe mit einer Quote von 7 Prozent, wobei die **Erwerbsteuer (USA)**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="20955-389">EU purchases at a rate of 7 percent, where the **Use tax** option is set to **Yes**.</span></span>  |
| <span data-ttu-id="20955-390">EUS</span><span class="sxs-lookup"><span data-stu-id="20955-390">EUS</span></span>                | <span data-ttu-id="20955-391">19</span><span class="sxs-lookup"><span data-stu-id="20955-391">19</span></span>             | <span data-ttu-id="20955-392">EU-Verkäufe, bei denen die **Befreit**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="20955-392">EU sales where the **Exempt** option is set to **Yes**.</span></span>                               |
| <span data-ttu-id="20955-393">THIRD</span><span class="sxs-lookup"><span data-stu-id="20955-393">THIRD</span></span>              | <span data-ttu-id="20955-394">19</span><span class="sxs-lookup"><span data-stu-id="20955-394">19</span></span>             | <span data-ttu-id="20955-395">Exportverkäufe, bei denen die **Befreit**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="20955-395">Export sales where the **Exempt** option is set to **Yes**.</span></span>                           |

2. <span data-ttu-id="20955-396">Auf der **Mehrwertsteuercodes**-Seite weisen Sie auf dem Inforegister **Berichtseinstellungen** den Mehrwertsteuercodes Berichtscodes zu.</span><span class="sxs-lookup"><span data-stu-id="20955-396">On the **Sales tax codes** page, on the **Report setup** FastTab, assign reporting codes to sales tax codes.</span></span>

<span data-ttu-id="20955-397">Die folgende Tabelle zeigt, wie Sie die Mehrwertsteuer-Berichtscodes den Mehrwertsteuercodes zuweisen.</span><span class="sxs-lookup"><span data-stu-id="20955-397">The following table shows how to assign the sales tax reporting codes to sales tax codes.</span></span>

| <span data-ttu-id="20955-398">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="20955-398">**Sales tax code**</span></span> | <span data-ttu-id="20955-399">**Steuerpflichtiger Umsatz**</span><span class="sxs-lookup"><span data-stu-id="20955-399">**Taxable sales**</span></span> | <span data-ttu-id="20955-400">**Steuerfreier Verkauf**</span><span class="sxs-lookup"><span data-stu-id="20955-400">**Tax-free sale**</span></span> | <span data-ttu-id="20955-401">**Mehrwertsteuer**</span><span class="sxs-lookup"><span data-stu-id="20955-401">**Sales tax payable**</span></span> | <span data-ttu-id="20955-402">**Steuerpflichtige Einkäufe**</span><span class="sxs-lookup"><span data-stu-id="20955-402">**Taxable purchases**</span></span> | <span data-ttu-id="20955-403">**Vorsteuer**</span><span class="sxs-lookup"><span data-stu-id="20955-403">**Sales tax receivable**</span></span> | <span data-ttu-id="20955-404">**Steuerpflichtiger Import**</span><span class="sxs-lookup"><span data-stu-id="20955-404">**Taxable import**</span></span> | <span data-ttu-id="20955-405">**Erwerbsteuer (USA)**</span><span class="sxs-lookup"><span data-stu-id="20955-405">**Use tax**</span></span> | <span data-ttu-id="20955-406">**Erwerbsteuerausgleich**</span><span class="sxs-lookup"><span data-stu-id="20955-406">**Offset use tax**</span></span> |
|--------------------|-------------------|-------------------|-----------------------|-----------------------|--------------------------|--------------------|-------------|--------------------|
| <span data-ttu-id="20955-407">VAT19</span><span class="sxs-lookup"><span data-stu-id="20955-407">VAT19</span></span>              | <span data-ttu-id="20955-408">81</span><span class="sxs-lookup"><span data-stu-id="20955-408">81</span></span>                |                   | <span data-ttu-id="20955-409">181</span><span class="sxs-lookup"><span data-stu-id="20955-409">181</span></span>                   |                       |                          |                    |             |                    |
| <span data-ttu-id="20955-410">VAT7</span><span class="sxs-lookup"><span data-stu-id="20955-410">VAT7</span></span>               | <span data-ttu-id="20955-411">86</span><span class="sxs-lookup"><span data-stu-id="20955-411">86</span></span>                |                   | <span data-ttu-id="20955-412">186</span><span class="sxs-lookup"><span data-stu-id="20955-412">186</span></span>                   |                       |                          |                    |             |                    |
| <span data-ttu-id="20955-413">InVAT19</span><span class="sxs-lookup"><span data-stu-id="20955-413">InVAT19</span></span>            |                   |                   |                       |                       | <span data-ttu-id="20955-414">66</span><span class="sxs-lookup"><span data-stu-id="20955-414">66</span></span>                       |                    |             |                    |
| <span data-ttu-id="20955-415">InVAT7</span><span class="sxs-lookup"><span data-stu-id="20955-415">InVAT7</span></span>             |                   |                   |                       |                       | <span data-ttu-id="20955-416">66</span><span class="sxs-lookup"><span data-stu-id="20955-416">66</span></span>                       |                    |             |                    |
| <span data-ttu-id="20955-417">EU19</span><span class="sxs-lookup"><span data-stu-id="20955-417">EU19</span></span>               |                   |                   |                       |                       |                          | <span data-ttu-id="20955-418">89</span><span class="sxs-lookup"><span data-stu-id="20955-418">89</span></span>                 | <span data-ttu-id="20955-419">189</span><span class="sxs-lookup"><span data-stu-id="20955-419">189</span></span>         | <span data-ttu-id="20955-420">61</span><span class="sxs-lookup"><span data-stu-id="20955-420">61</span></span>                 |
| <span data-ttu-id="20955-421">EU7</span><span class="sxs-lookup"><span data-stu-id="20955-421">EU7</span></span>                |                   |                   |                       |                       |                          | <span data-ttu-id="20955-422">93</span><span class="sxs-lookup"><span data-stu-id="20955-422">93</span></span>                 | <span data-ttu-id="20955-423">193</span><span class="sxs-lookup"><span data-stu-id="20955-423">193</span></span>         | <span data-ttu-id="20955-424">61</span><span class="sxs-lookup"><span data-stu-id="20955-424">61</span></span>                 |
| <span data-ttu-id="20955-425">EUS</span><span class="sxs-lookup"><span data-stu-id="20955-425">EUS</span></span>                |                   | <span data-ttu-id="20955-426">41</span><span class="sxs-lookup"><span data-stu-id="20955-426">41</span></span>                |                       |                       |                          |                    |             |                    |
| <span data-ttu-id="20955-427">THIRD</span><span class="sxs-lookup"><span data-stu-id="20955-427">THIRD</span></span>              |                   | <span data-ttu-id="20955-428">43</span><span class="sxs-lookup"><span data-stu-id="20955-428">43</span></span>                |                       |                       |                          |                    |             |                    |

> [!NOTE]
> <span data-ttu-id="20955-429">Die vorhergehende Konfiguration ist nur ein Beispiel und hängt von der Struktur der Mehrwertsteuercodes ab, die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="20955-429">The preceding configuration is just an example and depends on the structure of the sales tax codes that are used.</span></span> <span data-ttu-id="20955-430">Damit Werte für die Mehrwertsteuererklärung berechnet und übertragen werde, müssen Sie für jeden Steuercode, der im Mehrwertsteuerzahlungsprozess verwendet wird, einen entsprechenden Mehrwertsteuer-Erklärungscode in einem oder mehreren Feldern der Registerkarte **Berichteinstellung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="20955-430">If you want values to be calculated and transferred to the sales tax report, for each tax code that is used in the sales tax payment process, you must set a relevant sales tax reporting code in one or more fields on the **Report setup** FastTab.</span></span>

3. <span data-ttu-id="20955-431">Wechseln Sie zu **Steuer \> Einstellung \> Mehrwertsteuer \> Einrichtung der elektronischen Steuererklärung**.</span><span class="sxs-lookup"><span data-stu-id="20955-431">Go to **Tax \> Setup \> Sales tax \> Electronic tax declaration setup**.</span></span>
4. <span data-ttu-id="20955-432">Im Feld **Formatzuordnung** wählen Sie das Format **Elster (DE)** aus, das Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="20955-432">In the **Format mapping** field, select the **Elster (DE)** format that you downloaded earlier.</span></span>
5. <span data-ttu-id="20955-433">Führen Sie die folgenden Buchungen aus.</span><span class="sxs-lookup"><span data-stu-id="20955-433">Post the following transactions.</span></span> <span data-ttu-id="20955-434">Informationen zu Kundenrechnungen finden Sie beispielsweise unter **Debitorenkonten** \> **Rechnungen** \> **Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="20955-434">For example, for customer invoices, go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span> <span data-ttu-id="20955-435">Kreditorenrechnungen wechseln Sie zu **Kreditorenkonten \> Rechnungen \> Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="20955-435">For vendor invoices, go to **Accounts payable \> Invoices \> Invoice journal**.</span></span>

| <span data-ttu-id="20955-436">**Datum**</span><span class="sxs-lookup"><span data-stu-id="20955-436">**Date**</span></span>        | <span data-ttu-id="20955-437">**Buchungstyp**</span><span class="sxs-lookup"><span data-stu-id="20955-437">**Transaction type**</span></span>      | <span data-ttu-id="20955-438">**Nettobetrag**</span><span class="sxs-lookup"><span data-stu-id="20955-438">**Amount net**</span></span> | <span data-ttu-id="20955-439">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="20955-439">**VAT amount**</span></span> | <span data-ttu-id="20955-440">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="20955-440">**Sales tax code**</span></span> | <span data-ttu-id="20955-441">**Erwartete Steuerbemessungsgrundlage – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="20955-441">**Expected tax base – reporting code**</span></span> | <span data-ttu-id="20955-442">**Erwarteter Steuerbemessungsbetrag – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="20955-442">**Expected tax amount – reporting code**</span></span> |
|-----------------|---------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| <span data-ttu-id="20955-443">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="20955-443">January 1, 2020</span></span> | <span data-ttu-id="20955-444">Debitorenrechnung</span><span class="sxs-lookup"><span data-stu-id="20955-444">Customer invoice</span></span>          | <span data-ttu-id="20955-445">100</span><span class="sxs-lookup"><span data-stu-id="20955-445">100</span></span>            | <span data-ttu-id="20955-446">19</span><span class="sxs-lookup"><span data-stu-id="20955-446">19</span></span>             | <span data-ttu-id="20955-447">VAT19</span><span class="sxs-lookup"><span data-stu-id="20955-447">VAT19</span></span>              | <span data-ttu-id="20955-448">81</span><span class="sxs-lookup"><span data-stu-id="20955-448">81</span></span>                                     | <span data-ttu-id="20955-449">181</span><span class="sxs-lookup"><span data-stu-id="20955-449">181</span></span>                                      |
| <span data-ttu-id="20955-450">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="20955-450">January 1, 2020</span></span> | <span data-ttu-id="20955-451">Kreditorenrechnung (EU)</span><span class="sxs-lookup"><span data-stu-id="20955-451">Vendor invoice (EU)</span></span>       | <span data-ttu-id="20955-452">100</span><span class="sxs-lookup"><span data-stu-id="20955-452">100</span></span>            | <span data-ttu-id="20955-453">7</span><span class="sxs-lookup"><span data-stu-id="20955-453">7</span></span>              | <span data-ttu-id="20955-454">EU7</span><span class="sxs-lookup"><span data-stu-id="20955-454">EU7</span></span>                | <span data-ttu-id="20955-455">93</span><span class="sxs-lookup"><span data-stu-id="20955-455">93</span></span>                                     | <span data-ttu-id="20955-456">193 – Steuerpflichtig 61 – Steuerabzug</span><span class="sxs-lookup"><span data-stu-id="20955-456">193 – Tax payable 61 – Tax deduction</span></span>     |
| <span data-ttu-id="20955-457">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="20955-457">January 1, 2020</span></span> | <span data-ttu-id="20955-458">Debitorenrechnung (EU)</span><span class="sxs-lookup"><span data-stu-id="20955-458">Customer invoice (EU)</span></span>     | <span data-ttu-id="20955-459">100</span><span class="sxs-lookup"><span data-stu-id="20955-459">100</span></span>            | <span data-ttu-id="20955-460">0</span><span class="sxs-lookup"><span data-stu-id="20955-460">0</span></span>              | <span data-ttu-id="20955-461">EUS</span><span class="sxs-lookup"><span data-stu-id="20955-461">EUS</span></span>                | <span data-ttu-id="20955-462">41</span><span class="sxs-lookup"><span data-stu-id="20955-462">41</span></span>                                     | <span data-ttu-id="20955-463">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="20955-463">Not applicable</span></span>                           |
| <span data-ttu-id="20955-464">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="20955-464">January 1, 2020</span></span> | <span data-ttu-id="20955-465">Debitorenrechnung (Export)</span><span class="sxs-lookup"><span data-stu-id="20955-465">Customer invoice (export)</span></span> | <span data-ttu-id="20955-466">100</span><span class="sxs-lookup"><span data-stu-id="20955-466">100</span></span>            | <span data-ttu-id="20955-467">0</span><span class="sxs-lookup"><span data-stu-id="20955-467">0</span></span>              | <span data-ttu-id="20955-468">THIRD</span><span class="sxs-lookup"><span data-stu-id="20955-468">THIRD</span></span>              | <span data-ttu-id="20955-469">43</span><span class="sxs-lookup"><span data-stu-id="20955-469">43</span></span>                                     | <span data-ttu-id="20955-470">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="20955-470">Not applicable</span></span>                           |

6. <span data-ttu-id="20955-471">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="20955-471">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
7. <span data-ttu-id="20955-472">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder auf die angegebenen Werte ein.</span><span class="sxs-lookup"><span data-stu-id="20955-472">In the **Report sales tax for settlement period** dialog box, set the following fields to the specified values:</span></span>

    - <span data-ttu-id="20955-473">**Ausgleichsperiode:** Mo</span><span class="sxs-lookup"><span data-stu-id="20955-473">**Settlement period:** Mon</span></span>
    - <span data-ttu-id="20955-474">**Von Datum** = 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="20955-474">**From date:** 1/1/2020</span></span>

8. <span data-ttu-id="20955-475">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-475">Select **OK**.</span></span>
9. <span data-ttu-id="20955-476">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld wählen Sie das **Elektronisches Steuerdokument erstellen**-Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="20955-476">In the **German sales tax report** dialog box, select the **Create electronic tax document** check box.</span></span>
10. <span data-ttu-id="20955-477">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-477">Select **OK**.</span></span>
11. <span data-ttu-id="20955-478">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**, und wählen Sie die erforderliche Position aus.</span><span class="sxs-lookup"><span data-stu-id="20955-478">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**, and select the required line.</span></span>
12. <span data-ttu-id="20955-479">Auf der **Protokoll der elektronischen Steuererklärung**-Seite, wählen Sie die **Allgemein**-Registerkarte und überprüfen die allgemeinen Informationen.</span><span class="sxs-lookup"><span data-stu-id="20955-479">On the **Electronic tax declaration log** page, select the **General** tab, and review the general information.</span></span>

![Seite „Protokoll der elektronischen Steuererklärung“, Registerkarte „Allgemein“](media/2_Electronic_tax_declaration_log.png)

13. <span data-ttu-id="20955-481">Wählen Sie **Vorschau** aus, klicken Sie auf die Registerkarte und überprüfen Sie die gemeldeten Werte.</span><span class="sxs-lookup"><span data-stu-id="20955-481">Select the **Preview** tab, and review the reported values.</span></span>

![Vorschau des Protokolls der elektronischen Steuererklärung](media/3_Electronic_tax_declaration_log.png)

14. <span data-ttu-id="20955-483">Wählen Sie das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="20955-483">Select the paper clip symbol in the upper-right corner.</span></span>
15. <span data-ttu-id="20955-484">Wählen Sie **Öffnen** und überprüfen Sie die XML-Datei oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="20955-484">Select **Open** at the top of the page, and review the XML file.</span></span>

![XML-Datei](media/4_XML_file.png)

### <a name="correction-transactions"></a><span data-ttu-id="20955-486">Korrekturtransaktionen</span><span class="sxs-lookup"><span data-stu-id="20955-486">Correction transactions</span></span>

1.  <span data-ttu-id="20955-487">Wählen Sie eine neue Transaktion aus.</span><span class="sxs-lookup"><span data-stu-id="20955-487">Post a new transaction.</span></span> <span data-ttu-id="20955-488">Informationen zur Buchung einer Kundenrechnung finden Sie beispielsweise unter **Debitorenkonten** \> **Rechnungen** \> **Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="20955-488">For example, to post a customer invoice, go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>

| <span data-ttu-id="20955-489">**Datum**</span><span class="sxs-lookup"><span data-stu-id="20955-489">**Date**</span></span>        | <span data-ttu-id="20955-490">**Buchungstyp**</span><span class="sxs-lookup"><span data-stu-id="20955-490">**Transaction type**</span></span>        | <span data-ttu-id="20955-491">**Nettobetrag**</span><span class="sxs-lookup"><span data-stu-id="20955-491">**Amount net**</span></span> | <span data-ttu-id="20955-492">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="20955-492">**VAT amount**</span></span> | <span data-ttu-id="20955-493">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="20955-493">**Sales tax code**</span></span> | <span data-ttu-id="20955-494">**Erwartete Steuerbemessungsgrundlage – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="20955-494">**Expected tax base – Reporting code**</span></span> | <span data-ttu-id="20955-495">**Erwarteter Steuerbemessungsbetrag – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="20955-495">**Expected tax amount – Reporting code**</span></span> |
|-----------------|-----------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| <span data-ttu-id="20955-496">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="20955-496">January 1, 2020</span></span> | <span data-ttu-id="20955-497">Debitorenrechnung (Inland)</span><span class="sxs-lookup"><span data-stu-id="20955-497">Customer invoice (domestic)</span></span> | <span data-ttu-id="20955-498">100</span><span class="sxs-lookup"><span data-stu-id="20955-498">100</span></span>            | <span data-ttu-id="20955-499">7</span><span class="sxs-lookup"><span data-stu-id="20955-499">7</span></span>              | <span data-ttu-id="20955-500">VAT7</span><span class="sxs-lookup"><span data-stu-id="20955-500">VAT7</span></span>               | <span data-ttu-id="20955-501">86</span><span class="sxs-lookup"><span data-stu-id="20955-501">86</span></span>                                     | <span data-ttu-id="20955-502">186</span><span class="sxs-lookup"><span data-stu-id="20955-502">186</span></span>                                      |

2. <span data-ttu-id="20955-503">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="20955-503">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
3. <span data-ttu-id="20955-504">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder auf die angegebenen Werte ein.</span><span class="sxs-lookup"><span data-stu-id="20955-504">In the **Report sales tax for settlement period** dialog box, set the following fields to the specified values:</span></span>

    - <span data-ttu-id="20955-505">**Ausgleichsperiode:** Mo</span><span class="sxs-lookup"><span data-stu-id="20955-505">**Settlement period:** Mon</span></span>
    - <span data-ttu-id="20955-506">**Von Datum** = 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="20955-506">**From date:** 1/1/2020</span></span>

4. <span data-ttu-id="20955-507">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-507">Select **OK**.</span></span>
5. <span data-ttu-id="20955-508">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld wählen Sie das **Elektronisches Steuerdokument erstellen**-Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="20955-508">In the **German sales tax report** dialog box, select the **Create electronic tax document** check box.</span></span>
6. <span data-ttu-id="20955-509">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-509">Select **OK**.</span></span>
7. <span data-ttu-id="20955-510">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**, und wählen Sie die erforderliche Position aus.</span><span class="sxs-lookup"><span data-stu-id="20955-510">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**, and select the required line.</span></span>
8. <span data-ttu-id="20955-511">Wählen Sie **Vorschau** aus, klicken Sie auf die Registerkarte und überprüfen Sie die gemeldeten Werte.</span><span class="sxs-lookup"><span data-stu-id="20955-511">Select the **Preview** tab, and review the reported values.</span></span>

    ![Vorschau des Protokolls der elektronischen Steuererklärung](media/5_Electronic_tax_declaration_log.png)

    <span data-ttu-id="20955-513">Eine Korrekturbuchung ist der Erklärung anhand der Codes **86** und **83** hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="20955-513">A correction transaction is added to the declaration in codes **86** and **83**.</span></span>

9. <span data-ttu-id="20955-514">Wählen Sie das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="20955-514">Select the paper clip symbol in the upper-right corner.</span></span>
10. <span data-ttu-id="20955-515">Wählen Sie **Öffnen** und überprüfen Sie die XML-Datei oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="20955-515">Select **Open** at the top of the page, and review the XML file.</span></span>

    ![Zu überprüfende XML-Datei](media/6_XML_file.png)

    <span data-ttu-id="20955-517">Eine Korrekturbuchung ist der Erklärung anhand der Codes **86** und **83** hinzugefügt worden.</span><span class="sxs-lookup"><span data-stu-id="20955-517">A correction transaction is added to the declaration in codes **86** and **83**.</span></span>

## <a name="review-sales-tax-report-amounts"></a><span data-ttu-id="20955-518">Überprüfen Sie die Beträge des Umsatzsteuerberichts</span><span class="sxs-lookup"><span data-stu-id="20955-518">Review sales tax report amounts</span></span> 

<span data-ttu-id="20955-519">Sie können den Umsatzsteuerbetrag optional im SSRS-Bericht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="20955-519">You can optionally review sales tax amount in SSRS report.</span></span>

### <a name="set-up-the-report-layout-for-sales-tax-authorities"></a><span data-ttu-id="20955-520">Richten Sie das Berichtslayout für die Umsatzsteuerbehörden ein</span><span class="sxs-lookup"><span data-stu-id="20955-520">Set up the report layout for sales tax authorities</span></span>

1. <span data-ttu-id="20955-521">Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuerbehörden**.</span><span class="sxs-lookup"><span data-stu-id="20955-521">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax authorities**.</span></span>
2. <span data-ttu-id="20955-522">Wählen Sie auf der Seite **Mehrwertsteuer-Behörden** die Mehrwertsteuerbehörde, die für den Mehrwertsteuer-Abrechnungszeitraum in den Mehrwertsteuercodes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="20955-522">On the **Sales tax authorities** page, select the sales tax authority that will be used in the sales tax codes for the sales tax settlement period.</span></span>
3. <span data-ttu-id="20955-523">Im **Berichtslayout**-Feld wählen Sie **Deutsches Steuererklärungslayout**.</span><span class="sxs-lookup"><span data-stu-id="20955-523">In the **Report layout** field, select **German report layout**.</span></span>

### <a name="generate-a-sales-tax-payment-and-print-the-german-sales-tax-report"></a><a name="generatesalestaxpayment"></a> <span data-ttu-id="20955-524">Generieren Sie eine Mehrwertsteuerzahlung und drucken Sie den deutschen Mehrwertsteuerbericht aus</span><span class="sxs-lookup"><span data-stu-id="20955-524">Generate a sales tax payment and print the German sales tax report</span></span>

<span data-ttu-id="20955-525">Berechnen Sie am Ende des MwSt.-Berichtszeitraums die Mehrwertsteuerbeträge für den Abrechnungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="20955-525">At the end of the VAT reporting period, calculate the sales tax amounts for the settlement period.</span></span>

1. <span data-ttu-id="20955-526">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="20955-526">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
2. <span data-ttu-id="20955-527">Im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld stellen die erforderlichen Felder wie [vorhin](#createvatdecxmlformat) beschrieben ein.</span><span class="sxs-lookup"><span data-stu-id="20955-527">In the **Settle and post sales tax** dialog box, set the required fields as described [earlier](#createvatdecxmlformat).</span></span>
3. <span data-ttu-id="20955-528">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-528">Select **OK**.</span></span>
4. <span data-ttu-id="20955-529">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld legen Sie die **Elektronisches Steuerdokument erstellen**-Option auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="20955-529">In the **German sales tax report** dialog box, set the **Create electronic tax document** option to **No**.</span></span>
5. <span data-ttu-id="20955-530">Wählen Sie **OK** aus, um die Mehrwertsteuerzahlung zu generieren und den Bericht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="20955-530">Select **OK** to generate the sales tax payment and review the report.</span></span>

<span data-ttu-id="20955-531">Wenn Sie Transaktionen wie in Schritt 5 des [Beispiels](#example) zu Beginn dieses Themas buchen, werden die folgenden Daten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="20955-531">If you post transactions as described in step 5 of the [example](#example) earlier in this topic, you will see the following data.</span></span>

![Generierter deutscher Mehrwertsteuerbericht, Seite 1](media/7_Sales_tax_reporting.png)

![Generierter deutscher Mehrwertsteuerbericht, Seite 2](media/8_Sales_tax_reporting.png)

### <a name="print-a-sales-tax-payment-report-from-a-sales-tax-payment"></a><span data-ttu-id="20955-534">Drucken Sie einen Mehrwertsteuerzahlungsbericht aus einer Mehrwertsteuerzahlung</span><span class="sxs-lookup"><span data-stu-id="20955-534">Print a sales tax payment report from a sales tax payment</span></span>

1. <span data-ttu-id="20955-535">Wechseln Sie zu **Steuer** \> **Anfragen und Berichte** \> **Mehrwertsteuerzahlungen**.</span><span class="sxs-lookup"><span data-stu-id="20955-535">Go to **Tax** \> **Inquiries and reports** \> **Sales tax payments**.</span></span>
2. <span data-ttu-id="20955-536">Auf der **Mehrwertsteuerzahlung**-Seite wählen Sie den Datensatz aus und wählen dann **Bericht drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="20955-536">On the **Sales tax payment** page, select the record, and then select **Print report**.</span></span>
3. <span data-ttu-id="20955-537">Stellen Sie im Dialogfeld die Felder wie im vorherigen Abschnitt beschrieben ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-537">In the dialog box, set the fields as described in the previous section, and then select **OK**.</span></span>

### <a name="report-sales-tax-for-the-settlement-period"></a><span data-ttu-id="20955-538">Umsatzsteuer für Abrechnungszeitraum melden</span><span class="sxs-lookup"><span data-stu-id="20955-538">Report sales tax for the settlement period</span></span>

<span data-ttu-id="20955-539">Sie können den deutschen Mehrwertsteuerbericht auch mit der **Umsatzsteuer für Abrechnungszeitraum melden**-Anfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="20955-539">You can also generate the German sales tax report by using the **Report sales tax for settlement period** inquiry.</span></span>

1. <span data-ttu-id="20955-540">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="20955-540">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
2. <span data-ttu-id="20955-541">Im **Umsatzsteuer für Abrechnungszeitraum melden**-Dialogfeld, stellen Sie die **Ausgleichsperiode** und die **Anfangsdatum**-Felder wie im Abschnitt [Generieren Sie eine Mehrwertsteuerzahlung und drucken Sie den deutschen Mehrwertsteuerbericht aus](#generatesalestaxpayment) weiter oben in diesem Thema beschrieben ein.</span><span class="sxs-lookup"><span data-stu-id="20955-541">In the **Report sales tax for settlement period** dialog box, set the **Settlement period** and **From date** fields as described in the [Generate a sales tax payment and print the German sales tax report](#generatesalestaxpayment) section earlier in this topic.</span></span>
3. <span data-ttu-id="20955-542">Wählen Sie im Feld **Mehrwertsteuer, Zahlungsversion** einen der folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="20955-542">In the **Sales tax payment version** field, select one of the following values:</span></span>

- <span data-ttu-id="20955-543">**Original** – Einen Mehrwertsteuerbericht generieren für die erste gebuchte Ausgleichsberechnung für das Periodenintervall.</span><span class="sxs-lookup"><span data-stu-id="20955-543">**Original** – Generate a report for sales tax transactions of the first posted settlement calculation for the period.</span></span>
- <span data-ttu-id="20955-544">**Korrekturen** – Einen Mehrwertsteuerbericht generieren für nachfolgende Ausgleichsberechnungen für das Periodenintervall.</span><span class="sxs-lookup"><span data-stu-id="20955-544">**Corrections** – Generate a report for sales tax transactions of subsequent settlement calculations for the period.</span></span>
- <span data-ttu-id="20955-545">**Gesamtliste** – Erstellen Sie einen Bericht für alle Verkaufstransaktionen für den Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="20955-545">**Total list** – Generate a report for all sales transactions for the period.</span></span> <span data-ttu-id="20955-546">Diese Transaktionen umfassen ursprüngliche und korrigierte Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="20955-546">These transactions include original and corrected transactions.</span></span>

4. <span data-ttu-id="20955-547">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="20955-547">Select **OK**.</span></span>
5. <span data-ttu-id="20955-548">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="20955-548">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
6. <span data-ttu-id="20955-549">Wählen Sie im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Original** aus.</span><span class="sxs-lookup"><span data-stu-id="20955-549">In the **Settle and post sales tax** dialog box, in the **Sales tax payment version** field, select **Original**.</span></span>
7.  <span data-ttu-id="20955-550">Drucken Sie den Bericht aus und überprüfen Sie die Daten.</span><span class="sxs-lookup"><span data-stu-id="20955-550">Print the report, and review the data.</span></span>

| <span data-ttu-id="20955-551">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="20955-551">**Reporting code**</span></span> | <span data-ttu-id="20955-552">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="20955-552">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="20955-553">41</span><span class="sxs-lookup"><span data-stu-id="20955-553">41</span></span>                 | <span data-ttu-id="20955-554">100</span><span class="sxs-lookup"><span data-stu-id="20955-554">100</span></span>                  |
| <span data-ttu-id="20955-555">43</span><span class="sxs-lookup"><span data-stu-id="20955-555">43</span></span>                 | <span data-ttu-id="20955-556">100</span><span class="sxs-lookup"><span data-stu-id="20955-556">100</span></span>                  |
| <span data-ttu-id="20955-557">61</span><span class="sxs-lookup"><span data-stu-id="20955-557">61</span></span>                 | <span data-ttu-id="20955-558">7</span><span class="sxs-lookup"><span data-stu-id="20955-558">7</span></span>                    |
| <span data-ttu-id="20955-559">81</span><span class="sxs-lookup"><span data-stu-id="20955-559">81</span></span>                 | <span data-ttu-id="20955-560">100</span><span class="sxs-lookup"><span data-stu-id="20955-560">100</span></span>                  |
| <span data-ttu-id="20955-561">93</span><span class="sxs-lookup"><span data-stu-id="20955-561">93</span></span>                 | <span data-ttu-id="20955-562">100</span><span class="sxs-lookup"><span data-stu-id="20955-562">100</span></span>                  |
| <span data-ttu-id="20955-563">181</span><span class="sxs-lookup"><span data-stu-id="20955-563">181</span></span>                | <span data-ttu-id="20955-564">19</span><span class="sxs-lookup"><span data-stu-id="20955-564">19</span></span>                   |
| <span data-ttu-id="20955-565">193</span><span class="sxs-lookup"><span data-stu-id="20955-565">193</span></span>                | <span data-ttu-id="20955-566">7</span><span class="sxs-lookup"><span data-stu-id="20955-566">7</span></span>                    |

8. <span data-ttu-id="20955-567">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="20955-567">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
9. <span data-ttu-id="20955-568">Wählen Sie im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Neueste Korrekturen** aus.</span><span class="sxs-lookup"><span data-stu-id="20955-568">In the **Settle and post sales tax** dialog box, in the **Sales tax payment version** field, select **Latest corrections**.</span></span>
10. <span data-ttu-id="20955-569">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="20955-569">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
11. <span data-ttu-id="20955-570">Wählen Sie im **Mehrwertsteuer für Abrechnungszeitraum melden**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Korrekturen** aus.</span><span class="sxs-lookup"><span data-stu-id="20955-570">In the **Report sales tax for settlement period** dialog box, in the **Sales tax payment version** field, select **Corrections**.</span></span> <span data-ttu-id="20955-571">Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="20955-571">The following table shows the result.</span></span>

| <span data-ttu-id="20955-572">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="20955-572">**Reporting code**</span></span> | <span data-ttu-id="20955-573">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="20955-573">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="20955-574">86</span><span class="sxs-lookup"><span data-stu-id="20955-574">86</span></span>                 | <span data-ttu-id="20955-575">100</span><span class="sxs-lookup"><span data-stu-id="20955-575">100</span></span>                  |
| <span data-ttu-id="20955-576">186</span><span class="sxs-lookup"><span data-stu-id="20955-576">186</span></span>                | <span data-ttu-id="20955-577">7</span><span class="sxs-lookup"><span data-stu-id="20955-577">7</span></span>                    |

12. <span data-ttu-id="20955-578">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="20955-578">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
13. <span data-ttu-id="20955-579">Wählen Sie im **Mehrwertsteuer für Abrechnungszeitraum melden**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Gesamtliste** aus.</span><span class="sxs-lookup"><span data-stu-id="20955-579">In the **Report sales tax for settlement period** dialog box, in the **Sales tax payment version** field, select **Total list**.</span></span> <span data-ttu-id="20955-580">Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="20955-580">The following table shows the result.</span></span>

| <span data-ttu-id="20955-581">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="20955-581">**Reporting code**</span></span> | <span data-ttu-id="20955-582">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="20955-582">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="20955-583">41</span><span class="sxs-lookup"><span data-stu-id="20955-583">41</span></span>                 | <span data-ttu-id="20955-584">100</span><span class="sxs-lookup"><span data-stu-id="20955-584">100</span></span>                  |
| <span data-ttu-id="20955-585">43</span><span class="sxs-lookup"><span data-stu-id="20955-585">43</span></span>                 | <span data-ttu-id="20955-586">100</span><span class="sxs-lookup"><span data-stu-id="20955-586">100</span></span>                  |
| <span data-ttu-id="20955-587">61</span><span class="sxs-lookup"><span data-stu-id="20955-587">61</span></span>                 | <span data-ttu-id="20955-588">7</span><span class="sxs-lookup"><span data-stu-id="20955-588">7</span></span>                    |
| <span data-ttu-id="20955-589">81</span><span class="sxs-lookup"><span data-stu-id="20955-589">81</span></span>                 | <span data-ttu-id="20955-590">100</span><span class="sxs-lookup"><span data-stu-id="20955-590">100</span></span>                  |
| <span data-ttu-id="20955-591">86</span><span class="sxs-lookup"><span data-stu-id="20955-591">86</span></span>                 | <span data-ttu-id="20955-592">100</span><span class="sxs-lookup"><span data-stu-id="20955-592">100</span></span>                  |
| <span data-ttu-id="20955-593">93</span><span class="sxs-lookup"><span data-stu-id="20955-593">93</span></span>                 | <span data-ttu-id="20955-594">100</span><span class="sxs-lookup"><span data-stu-id="20955-594">100</span></span>                  |
| <span data-ttu-id="20955-595">181</span><span class="sxs-lookup"><span data-stu-id="20955-595">181</span></span>                | <span data-ttu-id="20955-596">19</span><span class="sxs-lookup"><span data-stu-id="20955-596">19</span></span>                   |
| <span data-ttu-id="20955-597">186</span><span class="sxs-lookup"><span data-stu-id="20955-597">186</span></span>                | <span data-ttu-id="20955-598">7</span><span class="sxs-lookup"><span data-stu-id="20955-598">7</span></span>                    |
| <span data-ttu-id="20955-599">193</span><span class="sxs-lookup"><span data-stu-id="20955-599">193</span></span>                | <span data-ttu-id="20955-600">7</span><span class="sxs-lookup"><span data-stu-id="20955-600">7</span></span>                    |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]