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
ms.sourcegitcommit: baab88d037ebf26e6c8822d96056e5ee475877aa
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2020
ms.locfileid: "3369575"
---
# <a name="vat-declaration-for-germany"></a><span data-ttu-id="becc7-103">Umsatzsteuererklärung für Deutschland</span><span class="sxs-lookup"><span data-stu-id="becc7-103">VAT declaration for Germany</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="becc7-104">In diesem Thema wird erläutert, wie Sie die Mehrwertsteuererklärung für juristische Personen in Deutschland einrichten und erstellen.</span><span class="sxs-lookup"><span data-stu-id="becc7-104">This topic explains how to set up and generate the value-added tax (VAT) declaration for legal entities in Germany.</span></span>

<span data-ttu-id="becc7-105">Weitere Informationen zur Einrichtung der Mehrwertsteuererklärung finden Sie unter [MwSt-Berichterstattung für Europa](emea-vat-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="becc7-105">For general information about how to set up the VAT statement, see [VAT reporting for Europe](emea-vat-reporting.md).</span></span>

## <a name="set-up-sales-tax-reporting-codes-for-vat-reporting"></a><span data-ttu-id="becc7-106">Mehrwertsteuer-Codes für Mehrwertsteuererklärung einrichten</span><span class="sxs-lookup"><span data-stu-id="becc7-106">Set up sales tax reporting codes for VAT reporting</span></span>

<span data-ttu-id="becc7-107">Richten Sie die Codes für die Mehrwertsteuererklärung ein, indem Sie die Anweisungen in [Mehrwertsteuer-Erklärungscodes einrichten](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="becc7-107">Set up sales tax reporting codes by following the instructions in [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).</span></span> <span data-ttu-id="becc7-108">Die folgende Tabelle enthält ein Beispiel für Umsatzsteuer-Berichtscodes für Deutschland.</span><span class="sxs-lookup"><span data-stu-id="becc7-108">The following table provides an example of sales tax reporting codes for Germany.</span></span>

<table width="614">
<thead>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-109"><strong>Code</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-109"><strong>Code</strong></span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-110"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-110"><strong>Description</strong></span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-111"><strong>Element in der XML-Datei der Umsatzsteuererklärung</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-111"><strong>Element in the XML file of the VAT declaration</strong></span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-112"><strong>Steuerbemessungsgrundlage oder Steuerbetrag</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-112"><strong>Tax base or tax amount</strong></span></span></p>
</td>
</tr>
</thead>
<tbody>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="becc7-113"><strong>Steuerfreier Verkauf mit Vorsteuerabzug für innergemeinschaftliche Lieferungen (&sect;4, Nr. 1b des UStG [Umsatzsteuergesetz</strong><strong> oder </strong><strong>Mehrwertsteuergesetz])</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-113"><strong>Tax-free sales with input tax deduction for intra-community supplies (&sect;4, no. 1, letter b of the UStG [Umsatzsteuergesetz</strong><strong>, or </strong><strong>VAT law])</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-114">41</span><span class="sxs-lookup"><span data-stu-id="becc7-114">41</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-115">Innergemeinschaftlicher Versand (&sect;4, Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-115">Intra-community shipment (&sect;4, no.</span></span> <span data-ttu-id="becc7-116">1b des UStG) für Kunden mit Steuerregistrierung.</span><span class="sxs-lookup"><span data-stu-id="becc7-116">1b of the UStG) to customers with tax registration.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-117">Kz41</span><span class="sxs-lookup"><span data-stu-id="becc7-117">Kz41</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-118">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-118">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-119">44</span><span class="sxs-lookup"><span data-stu-id="becc7-119">44</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-120">Innergemeinschaftliche Lieferungen von Neufahrzeugen an Kunden ohne Umsatzsteuer-Identifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="becc7-120">Intra-community deliveries of new vehicles to customers without a VAT ID.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-121">Kz44</span><span class="sxs-lookup"><span data-stu-id="becc7-121">Kz44</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-122">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-122">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-123">49</span><span class="sxs-lookup"><span data-stu-id="becc7-123">49</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-124">Innergemeinschaftliche Lieferungen von Neufahrzeugen außerhalb eines Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="becc7-124">Intra-community deliveries of new vehicles outside a company.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-125">Kz49</span><span class="sxs-lookup"><span data-stu-id="becc7-125">Kz49</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-126">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-126">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-127">43</span><span class="sxs-lookup"><span data-stu-id="becc7-127">43</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-128">Zusätzliche steuerfreie Verkäufe mit Vorsteuerabzug (z. B. Exporte).</span><span class="sxs-lookup"><span data-stu-id="becc7-128">Additional tax-free sales with input tax deduction (for example, exports).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-129">Kz43</span><span class="sxs-lookup"><span data-stu-id="becc7-129">Kz43</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-130">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-130">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="becc7-131"><strong>Steuerfreie Verkäufe ohne Vorsteuerabzug (z. B. Verkäufe nach &sect;4, Nr. 8 bis 28 des UStG)</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-131"><strong>Tax-free sales without input tax deduction (for example, sales according to &sect;4, no. 8 through 28 of the UStG)</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-132">48</span><span class="sxs-lookup"><span data-stu-id="becc7-132">48</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-133">Steuerfreier Verkauf ohne Vorsteuerabzug.</span><span class="sxs-lookup"><span data-stu-id="becc7-133">Tax-free sales without input tax deduction.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-134">Kz48</span><span class="sxs-lookup"><span data-stu-id="becc7-134">Kz48</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-135">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-135">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="becc7-136"><strong>Steuerpflichtiger Umsatz</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-136"><strong>Taxable sales</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-137">81</span><span class="sxs-lookup"><span data-stu-id="becc7-137">81</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-138">Steuerbemessungsgrundlage für Lieferungen oder Leistungen, die mit 19 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="becc7-138">Tax base for deliveries or services that are charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-139">Kz81</span><span class="sxs-lookup"><span data-stu-id="becc7-139">Kz81</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-140">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-140">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-141">181</span><span class="sxs-lookup"><span data-stu-id="becc7-141">181</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-142">Steuerbetrag für Lieferungen oder Leistungen, die mit 19 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="becc7-142">Tax amount for deliveries or services that are charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-143">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="becc7-143">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-144">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-144">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-145">86</span><span class="sxs-lookup"><span data-stu-id="becc7-145">86</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-146">Steuerbemessungsgrundlage für Lieferungen oder Leistungen, die mit 7 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="becc7-146">Tax base for deliveries or services that are charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-147">Kz86</span><span class="sxs-lookup"><span data-stu-id="becc7-147">Kz86</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-148">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-148">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-149">186</span><span class="sxs-lookup"><span data-stu-id="becc7-149">186</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-150">Steuerbetrag für Lieferungen oder Leistungen, die mit 7 Prozent berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="becc7-150">Tax amount for deliveries or services that are charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-151">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="becc7-151">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-152">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-152">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-153">35</span><span class="sxs-lookup"><span data-stu-id="becc7-153">35</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-154">Steuerbemessungsgrundlage für Lieferungen oder Leistungen zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="becc7-154">Tax base for deliveries or services at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-155">Kz35</span><span class="sxs-lookup"><span data-stu-id="becc7-155">Kz35</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-156">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-156">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-157">36</span><span class="sxs-lookup"><span data-stu-id="becc7-157">36</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-158">Steuerbetrag für Lieferungen oder Leistungen zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="becc7-158">Tax amount for deliveries or services at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-159">Kz36</span><span class="sxs-lookup"><span data-stu-id="becc7-159">Kz36</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-160">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-160">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-161">77</span><span class="sxs-lookup"><span data-stu-id="becc7-161">77</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-162">Lieferungen von land- und forstwirtschaftlichen Betrieben nach &sect;24 des UStG an Kunden mit einer Umsatzsteuer-Identifikationsnummer.</span><span class="sxs-lookup"><span data-stu-id="becc7-162">Deliveries of agricultural and forestry businesses, according to &sect;24 of the UStG, to customers who have a VAT ID.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-163">Kz77</span><span class="sxs-lookup"><span data-stu-id="becc7-163">Kz77</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-164">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-164">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-165">76</span><span class="sxs-lookup"><span data-stu-id="becc7-165">76</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-166">Steuerbemessungsgrundlage des Umsatzes, für den die Steuer zu zahlen ist &sect;24 des UStG (Sägewerksprodukte, Getränke und alkoholische Getränke wie Wein).</span><span class="sxs-lookup"><span data-stu-id="becc7-166">Tax base of turnover that tax is payable for, according to &sect;24 of the UStG (sawmill products, beverages and alcoholic liquids, such as wine).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-167">Kz76</span><span class="sxs-lookup"><span data-stu-id="becc7-167">Kz76</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-168">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-168">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-169">80</span><span class="sxs-lookup"><span data-stu-id="becc7-169">80</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-170">Steuerbetrag des Umsatzes, für den die Steuer zu zahlen ist &sect;24 des UStG (Sägewerksprodukte, Getränke und alkoholische Getränke wie Wein).</span><span class="sxs-lookup"><span data-stu-id="becc7-170">Tax amount of turnover that tax is payable for, according to &sect;24 of the UStG (sawmill products, beverages and alcoholic liquids, such as wine).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-171">Kz80</span><span class="sxs-lookup"><span data-stu-id="becc7-171">Kz80</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-172">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-172">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="becc7-173"><strong>Innergemeinschaftliche Akquisitionen und Mehrwertsteuer für solche Akquisitionen</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-173"><strong>Intra-community acquisitions and VAT payable for such acquisitions</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-174">91</span><span class="sxs-lookup"><span data-stu-id="becc7-174">91</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-175">Steuerfreie innergemeinschaftliche Akquisitionen.</span><span class="sxs-lookup"><span data-stu-id="becc7-175">Tax-free intra-community acquisitions.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-176">Kz91</span><span class="sxs-lookup"><span data-stu-id="becc7-176">Kz91</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-177">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-177">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-178">89</span><span class="sxs-lookup"><span data-stu-id="becc7-178">89</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-179">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="becc7-179">Tax base for the acquisition of goods from countries in the European Union (EU), charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-180">Kz89</span><span class="sxs-lookup"><span data-stu-id="becc7-180">Kz89</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-181">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-181">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-182">189</span><span class="sxs-lookup"><span data-stu-id="becc7-182">189</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-183">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="becc7-183">Tax amount for the acquisition of goods from countries in the EU, charged at 19 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-184">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="becc7-184">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-185">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-185">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-186">93</span><span class="sxs-lookup"><span data-stu-id="becc7-186">93</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-187">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="becc7-187">Tax base for the acquisition of goods from countries in the EU, charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-188">Kz93</span><span class="sxs-lookup"><span data-stu-id="becc7-188">Kz93</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-189">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-189">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-190">193</span><span class="sxs-lookup"><span data-stu-id="becc7-190">193</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-191">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="becc7-191">Tax amount for the acquisition of goods from countries in the EU, charged at 7 percent.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-192">Wird in der XML-Datei nicht separat angezeigt, aber insgesamt berücksichtigt (Kz83)</span><span class="sxs-lookup"><span data-stu-id="becc7-192">Not shown separately in the XML file but considered in the total (Kz83)</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-193">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-193">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-194">95</span><span class="sxs-lookup"><span data-stu-id="becc7-194">95</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-195">Steuerbemessungsgrundlage für den Erwerb von Waren aus Ländern der Europäischen Union (EU) zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="becc7-195">Tax base for the acquisition of goods from countries in the EU at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-196">Kz95</span><span class="sxs-lookup"><span data-stu-id="becc7-196">Kz95</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-197">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-197">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-198">98</span><span class="sxs-lookup"><span data-stu-id="becc7-198">98</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-199">Steuerbetrag für den Erwerb von Waren aus Ländern der Europäischen Union (EU) zu anderen Steuersätzen.</span><span class="sxs-lookup"><span data-stu-id="becc7-199">Tax amount for the acquisition of goods from countries in the EU at other tax rates.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-200">Kz98</span><span class="sxs-lookup"><span data-stu-id="becc7-200">Kz98</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-201">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-201">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-202">94</span><span class="sxs-lookup"><span data-stu-id="becc7-202">94</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-203">Steuerbemessungsgrundlage für innergemeinschaftliche Anschaffungen neuer Fahrzeuge (&sect;1b, Absätze 2 und 3 des UStG) von Lieferanten ohne MwSt.-ID zum allgemeinen Steuersatz.</span><span class="sxs-lookup"><span data-stu-id="becc7-203">Tax base for intra-community acquisitions of new vehicles (&sect;1b, paragraphs 2 and 3 of the UStG) from suppliers without a VAT ID, at the general tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-204">Kz94</span><span class="sxs-lookup"><span data-stu-id="becc7-204">Kz94</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-205">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-205">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-206">96</span><span class="sxs-lookup"><span data-stu-id="becc7-206">96</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-207">Steuerbetrag für innergemeinschaftliche Anschaffungen neuer Fahrzeuge (&sect;1b, Absätze 2 und 3 des UStG) von Lieferanten ohne MwSt.-ID zum allgemeinen Steuersatz.</span><span class="sxs-lookup"><span data-stu-id="becc7-207">Tax amount for intra-community acquisitions of new vehicles (&sect;1b, paragraphs 2 and 3 of the UStG) from suppliers without a VAT ID, at the general tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-208">Kz96</span><span class="sxs-lookup"><span data-stu-id="becc7-208">Kz96</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-209">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-209">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="becc7-210"><strong>Zusätzliche Informationen zum Vertrieb</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-210"><strong>Additional information about sales</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-211">42</span><span class="sxs-lookup"><span data-stu-id="becc7-211">42</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-212">Lieferungen des ersten Kunden für gemeinschaftsinterne Dreieckstransaktionen (&sect;25b des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-212">Deliveries by the first customer for intra-community triangular transactions (&sect;25b of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-213">Kz42</span><span class="sxs-lookup"><span data-stu-id="becc7-213">Kz42</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-214">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-214">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-215">60</span><span class="sxs-lookup"><span data-stu-id="becc7-215">60</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-216">Steuerpflichtiger Umsatz des ausführenden Unternehmers, für den der Leistungsempfänger die Steuer schuldet, gemäß &sect;13b (5) des UStG.</span><span class="sxs-lookup"><span data-stu-id="becc7-216">Taxable sales of the performing entrepreneur that the service recipient owes the tax for, according to &sect;13b (5) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-217">Kz60</span><span class="sxs-lookup"><span data-stu-id="becc7-217">Kz60</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-218">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-218">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-219">21</span><span class="sxs-lookup"><span data-stu-id="becc7-219">21</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-220">Sonstige nicht steuerpflichtige Dienstleistungen gemäß &sect;18b, Satz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-220">Other non-taxable services according to &sect;18b, sentence 1, no.</span></span> <span data-ttu-id="becc7-221">2 des UStG.</span><span class="sxs-lookup"><span data-stu-id="becc7-221">2 of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-222">Kz21</span><span class="sxs-lookup"><span data-stu-id="becc7-222">Kz21</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-223">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-223">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-224">45</span><span class="sxs-lookup"><span data-stu-id="becc7-224">45</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-225">Sonstige nicht steuerpflichtige Verkäufe (wenn der Erfüllungsort nicht in Deutschland liegt).</span><span class="sxs-lookup"><span data-stu-id="becc7-225">Other non-taxable sales (where the place of performance isn't in Germany).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-226">Kz45</span><span class="sxs-lookup"><span data-stu-id="becc7-226">Kz45</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-227">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-227">Tax base</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="becc7-228"><strong>Begünstigter als Steuerschuldner (&sect;13b des UStG)</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-228"><strong>Beneficiary as tax debtor (&sect;13b of the UStG)</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-229">46</span><span class="sxs-lookup"><span data-stu-id="becc7-229">46</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-230">Steuerbemessungsgrundlage für sonstige Leistungen gemäß &sect;3A (2) UStG eines Unternehmers, der sich im Rest der Gemeinde befindet (&sect;13b (1) des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-230">Tax base for other services in accordance with &sect;3a (2) UStG of an entrepreneur that is located in the rest of the community (&sect;13b (1) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-231">Kz46</span><span class="sxs-lookup"><span data-stu-id="becc7-231">Kz46</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-232">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-232">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-233">47</span><span class="sxs-lookup"><span data-stu-id="becc7-233">47</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-234">Steuerbetrag für sonstige Leistungen gemäß &sect;3A (2) UStG eines Unternehmers, der sich im Rest der Gemeinde befindet (&sect;13b (1) des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-234">Tax amount for other services in accordance with &sect;3a (2) UStG of an entrepreneur that is located in the rest of the community (&sect;13b (1) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-235">Kz47</span><span class="sxs-lookup"><span data-stu-id="becc7-235">Kz47</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-236">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-236">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-237">73</span><span class="sxs-lookup"><span data-stu-id="becc7-237">73</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-238">Steuerbemessungsgrundlage des Umsatzes, der unter das Grundsteuergesetz fällt &ndash; insbesondere Lieferungen von Grundstücken, für die sich der ausführende Unternehmer für eine Steuerschuld gemäß &sect;9 (3) des UStG entschieden hat.</span><span class="sxs-lookup"><span data-stu-id="becc7-238">Tax base of turnover that is covered by the property transfer tax law &ndash; in particular, deliveries of land for which the performing entrepreneur has opted for tax liability in accordance with &sect;9 (3) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-239">Kz73</span><span class="sxs-lookup"><span data-stu-id="becc7-239">Kz73</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-240">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-240">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-241">74</span><span class="sxs-lookup"><span data-stu-id="becc7-241">74</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-242">Steuerbetrag des Umsatzes, der unter das Grundsteuergesetz fällt &ndash; insbesondere Lieferungen von Grundstücken, für die sich der ausführende Unternehmer für eine Steuerschuld gemäß &sect;9 (3) des UStG entschieden hat.</span><span class="sxs-lookup"><span data-stu-id="becc7-242">Tax amount of turnover that is covered by the property transfer tax law &ndash; in particular, deliveries of land for which the performing entrepreneur has opted for tax liability in accordance with &sect;9 (3) of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-243">Kz74</span><span class="sxs-lookup"><span data-stu-id="becc7-243">Kz74</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-244">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-244">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-245">84</span><span class="sxs-lookup"><span data-stu-id="becc7-245">84</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-246">Steuerbemessungsgrundlage für andere Dienstleistungen (&sect;13b (2), Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-246">Tax base of other services (&sect;13b (2), no.</span></span> <span data-ttu-id="becc7-247">1, 2 und 4 bis 11 des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-247">1, 2, and 4 through 11 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-248">Kz84</span><span class="sxs-lookup"><span data-stu-id="becc7-248">Kz84</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-249">Steuerbasis</span><span class="sxs-lookup"><span data-stu-id="becc7-249">Tax base</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-250">85</span><span class="sxs-lookup"><span data-stu-id="becc7-250">85</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-251">Steuerbetrag für andere Dienstleistungen (&sect;13b (2), Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-251">Tax amount of other services (&sect;13b (2), no.</span></span> <span data-ttu-id="becc7-252">1, 2 und 4 bis 11 des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-252">1, 2, and 4 through 11 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-253">Kz85</span><span class="sxs-lookup"><span data-stu-id="becc7-253">Kz85</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-254">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-254">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="becc7-255"><strong>Abzugsfähige Vorsteuerbeträge</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-255"><strong>Deductible input tax amounts</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-256">66</span><span class="sxs-lookup"><span data-stu-id="becc7-256">66</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-257">Steuer auf Eingaben aus Rechnungen anderer Unternehmen (&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-257">Tax on input from invoices of other companies (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="becc7-258">1 des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-258">1 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-259">Kz66</span><span class="sxs-lookup"><span data-stu-id="becc7-259">Kz66</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-260">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-260">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-261">61</span><span class="sxs-lookup"><span data-stu-id="becc7-261">61</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-262">Vorsteuerbetrag aus innergemeinschaftlichen Erwerb von Gegenständen (&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-262">Input VAT amount from intra-community acquisitions of objects (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="becc7-263">3 des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-263">3 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-264">Kz61</span><span class="sxs-lookup"><span data-stu-id="becc7-264">Kz61</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-265">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-265">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-266">62</span><span class="sxs-lookup"><span data-stu-id="becc7-266">62</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-267">Anfallender Umsatzsteuerimport(&sect;15, Absatz 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-267">Import sales tax that is incurred (&sect;15, paragraph 1, no.</span></span> <span data-ttu-id="becc7-268">2 des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-268">2 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-269">Kz62</span><span class="sxs-lookup"><span data-stu-id="becc7-269">Kz62</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-270">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-270">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-271">67</span><span class="sxs-lookup"><span data-stu-id="becc7-271">67</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-272">Vorsteuerbeträge aus Dienstleistungen im Sinne von &sect;13b des UStG (&sect;15, Absatz 1, Klausel 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-272">Input tax amounts from services within the meaning of &sect;13b of the UStG (&sect;15, paragraph 1, clause 1, no.</span></span> <span data-ttu-id="becc7-273">4 des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-273">4 of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-274">Kz67</span><span class="sxs-lookup"><span data-stu-id="becc7-274">Kz67</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-275">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-275">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-276">63</span><span class="sxs-lookup"><span data-stu-id="becc7-276">63</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-277">Vorsteuerbeträge, die nach allgemeinen Durchschnittssätzen berechnet werden (&sect;23 und &sect;23A des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-277">Input tax amounts that are calculated according to general average rates (&sect;23 and &sect;23a of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-278">Kz63</span><span class="sxs-lookup"><span data-stu-id="becc7-278">Kz63</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-279">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-279">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-280">64</span><span class="sxs-lookup"><span data-stu-id="becc7-280">64</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-281">Korrektur des Vorsteuerabzugs (&sect;15A des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-281">Correction of input tax deduction (&sect;15a of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-282">Kz64</span><span class="sxs-lookup"><span data-stu-id="becc7-282">Kz64</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-283">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-283">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-284">59</span><span class="sxs-lookup"><span data-stu-id="becc7-284">59</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-285">Vorsteuerabzug für innergemeinschaftliche Lieferungen neuer Fahrzeuge außerhalb eines Unternehmens (&sect;2A des UStG) und Kleinunternehmen im Sinne von &sect;19 (1) des UStG (&sect;15 (4A) des UStG).</span><span class="sxs-lookup"><span data-stu-id="becc7-285">Input tax deduction for intra-community deliveries of new vehicles outside a company (&sect;2a of the UStG) and small businesses within the meaning of &sect;19 (1) of the UStG (&sect;15 (4a) of the UStG).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-286">Kz59</span><span class="sxs-lookup"><span data-stu-id="becc7-286">Kz59</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-287">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-287">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td colspan="4" width="614">
<p><span data-ttu-id="becc7-288"><strong>Sonstige Steuerbeträge</strong></span><span class="sxs-lookup"><span data-stu-id="becc7-288"><strong>Other tax amounts</strong></span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-289">65</span><span class="sxs-lookup"><span data-stu-id="becc7-289">65</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-290">Steuern aufgrund von Änderungen in der Form der Besteuerung und Nachsteuer auf besteuerte Anzahlungen usw. aufgrund von Änderungen des Steuersatzes.</span><span class="sxs-lookup"><span data-stu-id="becc7-290">Tax because of changes in the form of taxation, and after-tax on taxed down payments, and so on, because of changes in tax rate.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-291">Kz65</span><span class="sxs-lookup"><span data-stu-id="becc7-291">Kz65</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-292">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-292">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-293">69</span><span class="sxs-lookup"><span data-stu-id="becc7-293">69</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-294">Steuerbeträge, die auf Rechnungen falsch oder unplausibel ausgewiesen sind (&sect;14c des UStG) sowie Steuerbeträge, die in Übereinstimmung mit &sect;6A (4), Satz 2; &sect;17 (1), Satz 6 und &sect;25b (2) des UStG <strong>geschuldet</strong> sind oder <strong>geschuldete Steuerbeträge</strong> von einem Outsourcer oder Lagerhalter gemäß &sect;13A (2) 1, Nr.</span><span class="sxs-lookup"><span data-stu-id="becc7-294">Tax amounts that are shown incorrectly or unjustifiably on invoices (&sect;14c of the UStG), and also tax amounts that are <strong>owed</strong> in accordance with &sect;6a (4), sentence 2; &sect;17 (1), sentence 6; and &sect;25b (2) of the UStG, or <strong>tax amounts that are owed</strong> by an outsourcer or warehouse keeper in accordance with &sect;13a (2) 1, no.</span></span> <span data-ttu-id="becc7-295">6 des UStG.</span><span class="sxs-lookup"><span data-stu-id="becc7-295">6 of the UStG.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-296">Kz69</span><span class="sxs-lookup"><span data-stu-id="becc7-296">Kz69</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-297">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-297">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-298">39</span><span class="sxs-lookup"><span data-stu-id="becc7-298">39</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-299">Abzug der vereinbarten Sondervorauszahlung für eine langfristige Verlängerung (die in der Regel erst in der letzten Vorankündigung des Steuerzeitraums erfolgt).</span><span class="sxs-lookup"><span data-stu-id="becc7-299">Deduction of the stipulated special advance payment for long-term extension (which usually will be completed only in the last advance notification of the taxation period).</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-300">Kz39</span><span class="sxs-lookup"><span data-stu-id="becc7-300">Kz39</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-301">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-301">Tax amount</span></span></p>
</td>
</tr>
<tr>
<td width="75">
<p><span data-ttu-id="becc7-302">83</span><span class="sxs-lookup"><span data-stu-id="becc7-302">83</span></span></p>
</td>
<td width="340">
<p><span data-ttu-id="becc7-303">Gesamtbetrag der Mehrwertsteuer (Mehrwertsteuer-Vorauszahlung oder Mehrwertsteuerüberschuss).</span><span class="sxs-lookup"><span data-stu-id="becc7-303">Total VAT amount (VAT advance payment or VAT surplus).</span></span></p>
<p><span data-ttu-id="becc7-304">Bei der Umsatzsteuererklärung im XML-Format wird der Wert in diesem Feld automatisch als Summe der Berichtscodes 181, 186, 36, 80, 189, 193, 98, 96, 47, 74 und 85 abzüglich der Berichtscodes 66, 61, 62, 67, 63, 64, 59, 69 und 39 berechnet.</span><span class="sxs-lookup"><span data-stu-id="becc7-304">On the VAT declaration in XML format, the value in this box is automatically calculated as the sum of reporting codes 181, 186, 36, 80, 189, 193, 98, 96, 47, 74, and 85, minus reporting codes 66, 61, 62, 67, 63, 64, 59, 69, and 39.</span></span></p>
</td>
<td width="95">
<p><span data-ttu-id="becc7-305">Kz83</span><span class="sxs-lookup"><span data-stu-id="becc7-305">Kz83</span></span></p>
</td>
<td width="104">
<p><span data-ttu-id="becc7-306">USt.-Betrag</span><span class="sxs-lookup"><span data-stu-id="becc7-306">Tax amount</span></span></p>
</td>
</tr>
</tbody>
</table>
<p>&nbsp;</p>
<p>&nbsp;</p>

> [!NOTE]
> <span data-ttu-id="becc7-307">Beispiele für Formen von Mehrwertsteuererklärungen, die Deklarationszeilencodes enthalten, finden Sie unter [Formulare im Mehrwertsteuerverfahren für das Jahr 2020](https://umsatzsteuer-voranmeldung-2020.taxpool.net/Umsatzsteuer-Voranmeldung-2020.pdf).</span><span class="sxs-lookup"><span data-stu-id="becc7-307">For sample forms of advance VAT returns that include declaration row codes, see [Forms in the VAT procedure for the year 2020](https://umsatzsteuer-voranmeldung-2020.taxpool.net/Umsatzsteuer-Voranmeldung-2020.pdf).</span></span>

## <a name="set-up-sales-tax-codes"></a><span data-ttu-id="becc7-308">Mehrwertsteuercodes einrichten</span><span class="sxs-lookup"><span data-stu-id="becc7-308">Set up sales tax codes</span></span>

<span data-ttu-id="becc7-309">Richten Sie die Codes für die Mehrwertsteuererklärung ein, indem Sie die Anweisungen in [Mehrwertsteuercodes für MwSt-Berichterstattung](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) und [Mehrwertsteuerübersicht](../general-ledger/indirect-taxes-overview.md) befolgen.</span><span class="sxs-lookup"><span data-stu-id="becc7-309">Set up sales tax codes by following the instructions in [Sales tax codes for VAT reporting](emea-vat-reporting.md#sales-tax-codes-for-vat-reporting) and [Sales tax overview](../general-ledger/indirect-taxes-overview.md).</span></span>

> [!NOTE]
> <span data-ttu-id="becc7-310">In einer deutschen juristischen Entität sollten Umsatzsteuerkennzeichen für steuerfreie Verkäufe nach folgenden Regeln eingerichtet werden:</span><span class="sxs-lookup"><span data-stu-id="becc7-310">In a German legal entity, sales tax codes for tax-free sales should be set up according to the following rules:</span></span>
>
> - <span data-ttu-id="becc7-311">Der Steuersatz beträgt mehr als 0 (Null).</span><span class="sxs-lookup"><span data-stu-id="becc7-311">The tax rate is more than 0 (zero).</span></span>
> - <span data-ttu-id="becc7-312">Das Steuerkennzeichen ist als **Befreit** auf der **Umsatzsteuergruppen**-Seite gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="becc7-312">The tax code is marked as **Exempt** on the **Sales tax groups** page.</span></span>

## <a name="create-a-vat-declaration-in-xml-format"></a><a name= "createvatdecxmlformat"></a><span data-ttu-id="becc7-313">Erstellen einer Umsatzsteuererklärung im XML-Format</span><span class="sxs-lookup"><span data-stu-id="becc7-313">Create a VAT declaration in XML format</span></span>

1. <span data-ttu-id="becc7-314">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in der **Bibliothek der freigegebenen Anlagen** laden Sie die neuesten Versionen der Konfigurationen für die elektronische Berichterstattung (ER) für das Format der Umsatzsteuererklärung herunter:</span><span class="sxs-lookup"><span data-stu-id="becc7-314">In [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/V2), in the **Shared asset library**, download the latest versions of the Electronic reporting (ER) configurations for the VAT declaration format:</span></span>

    - <span data-ttu-id="becc7-315">**Elster (DE)**</span><span class="sxs-lookup"><span data-stu-id="becc7-315">**Elster (DE)**</span></span>

    <span data-ttu-id="becc7-316">Weitere Informationen finden Sie unter [Elektronische Berichtskonfigurationen aus Lifecycle Services herunterladen](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span><span class="sxs-lookup"><span data-stu-id="becc7-316">For more information, see [Download Electronic reporting configurations from Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).</span></span>

2. <span data-ttu-id="becc7-317">Wechseln Sie zu **Steuer** \> **Einstellungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer-Erklärungscodes**.</span><span class="sxs-lookup"><span data-stu-id="becc7-317">Go to **Tax** \> **Setup** \> **Sales tax** \> **Electronic tax declaration setup**.</span></span>
3. <span data-ttu-id="becc7-318">Im Feld **Formatzuordnung** wählen Sie das Format **Elster (DE)** aus, das Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="becc7-318">In the **Format mapping** field, select the **Elster (DE)** format that you downloaded earlier.</span></span>
4. <span data-ttu-id="becc7-319">Wechseln Sie zu **Steuer \> Erklärungen \> Mehrwertsteuer \> Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="becc7-319">Go to **Tax \> Declarations \> Sales tax \> Report sales tax for settlement period**.</span></span>
5. <span data-ttu-id="becc7-320">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="becc7-320">In the **Report sales tax for settlement period** dialog box, set the following fields.</span></span>

| <span data-ttu-id="becc7-321">**Feld**</span><span class="sxs-lookup"><span data-stu-id="becc7-321">**Field**</span></span>                 | <span data-ttu-id="becc7-322">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="becc7-322">**Description**</span></span>                                                                                                                                                                                                                                                                         |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="becc7-323">Ausgleichsperiode</span><span class="sxs-lookup"><span data-stu-id="becc7-323">Settlement period</span></span>         | <span data-ttu-id="becc7-324">Wählen Sie den gewünschten Berichtszeitraum aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-324">Select the applicable reporting period.</span></span>                                                                                                                                                                                                                                                 |
| <span data-ttu-id="becc7-325">Startdatum</span><span class="sxs-lookup"><span data-stu-id="becc7-325">From date</span></span>                 | <span data-ttu-id="becc7-326">Geben Sie das erste Datum des zu berechnenden Mehrwertsteuer-Abrechnungszeitraums an, um die Mehrwertsteuer zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="becc7-326">Enter the first date of the sales tax settlement period that sales tax should be calculated for.</span></span> <span data-ttu-id="becc7-327">Dieser Wert entspricht dem Datum im Feld **Vom** auf der **Mehrwertsteuer-Abrechnungszeitraum**-Seite.</span><span class="sxs-lookup"><span data-stu-id="becc7-327">This value corresponds to the date in the **From** field on the **Sales tax settlement periods** page.</span></span>                                                                                 |
| <span data-ttu-id="becc7-328">Buchungsdatum</span><span class="sxs-lookup"><span data-stu-id="becc7-328">Transaction date</span></span>          | <span data-ttu-id="becc7-329">Geben Sie das Datum an, für das die Mehrwertsteuererklärung berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="becc7-329">Enter the date when the sales tax report is calculated.</span></span> <span data-ttu-id="becc7-330">Der aktuelle Wert ist das aktuelle Datum.</span><span class="sxs-lookup"><span data-stu-id="becc7-330">The default value is the current date.</span></span> <span data-ttu-id="becc7-331">Die Mehrwertsteuerzahlung wird für alle Buchungen berechnet, die im Abrechnungszeitraum gebucht wurden.</span><span class="sxs-lookup"><span data-stu-id="becc7-331">The sales tax payment is calculated for all transactions that were posted during the settlement period.</span></span>                                                                                  |
| <span data-ttu-id="becc7-332">Mehrwertsteuer, Zahlungsversion</span><span class="sxs-lookup"><span data-stu-id="becc7-332">Sales tax payment version</span></span> | <span data-ttu-id="becc7-333">Wählen Sie den Mehrwertsteuer-Ausgleichstyp.</span><span class="sxs-lookup"><span data-stu-id="becc7-333">Select the type of sales tax settlement.</span></span> <span data-ttu-id="becc7-334">Wenn diese Umsatzsteuerabrechnung die erste Umsatzsteuerabrechnung für den Zeitraum ist, wählen Sie **Original**.</span><span class="sxs-lookup"><span data-stu-id="becc7-334">If this sales tax settlement is the first sales tax settlement for the period, select **Original**.</span></span> <span data-ttu-id="becc7-335">Wenn bereits eine Umsatzsteuerabrechnung generiert wurde, wählen Sie **Neueste Korrekturen**.</span><span class="sxs-lookup"><span data-stu-id="becc7-335">If a sales tax settlement has already been generated, select **Latest corrections**.</span></span> <span data-ttu-id="becc7-336">Weitere Informationen finden Sie unter [Eine Mehrwertsteuerzahlung erstellen](../general-ledger/tasks/create-sales-tax-payment.md).</span><span class="sxs-lookup"><span data-stu-id="becc7-336">For more information, see [Create a sales tax payment](../general-ledger/tasks/create-sales-tax-payment.md).</span></span> |

6. <span data-ttu-id="becc7-337">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-337">Select **OK**.</span></span>
7. <span data-ttu-id="becc7-338">Im Dialogfeld **Deutsche Mehrwertsteuererklärung** stellen Sie die folgenden Felder ein.</span><span class="sxs-lookup"><span data-stu-id="becc7-338">In the **German sales tax report** dialog box, set the following fields.</span></span>

| <span data-ttu-id="becc7-339">**Feld**</span><span class="sxs-lookup"><span data-stu-id="becc7-339">**Field**</span></span>                      | <span data-ttu-id="becc7-340">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="becc7-340">**Description**</span></span>                                                                                                                                                 |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="becc7-341">Elektronisches Steuerdokument erstellen</span><span class="sxs-lookup"><span data-stu-id="becc7-341">Create electronic tax document</span></span> | <span data-ttu-id="becc7-342">Setzen Sie diese Option auf **Ja**, um ein elektronisches Dokument zu erstellen, das die Details des Berichts enthält.</span><span class="sxs-lookup"><span data-stu-id="becc7-342">Set this option to **Yes** to create an electronic document that contains the details of the report.</span></span>                                                            |
| <span data-ttu-id="becc7-343">Separat übermittelte Dokumente</span><span class="sxs-lookup"><span data-stu-id="becc7-343">Documents submitted separately</span></span> | <span data-ttu-id="becc7-344">Setzen Sie diese Option auf **Ja**, wenn der gedruckte Bericht nicht zusammen mit dem elektronischen Dokument eingereicht wird.</span><span class="sxs-lookup"><span data-stu-id="becc7-344">Set this option to **Yes** if the printed report isn't submitted together with the electronic document.</span></span> <span data-ttu-id="becc7-345">In der XML-Datei sollte der Code Kz22 den Wert **1** haben.</span><span class="sxs-lookup"><span data-stu-id="becc7-345">In the XML file, code Kz22 should have the value **1**.</span></span> |

8. <span data-ttu-id="becc7-346">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-346">Select **OK**.</span></span> <span data-ttu-id="becc7-347">Auf der **Elektronisches Steuererklärungsprotokoll**-Seite (**Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**) wird eine neue Zeile erstellt.</span><span class="sxs-lookup"><span data-stu-id="becc7-347">A new line is created on the **Electronic tax declaration log** page (**Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**).</span></span>

![Seite „Protokoll der elektronischen Steuererklärung“](media/1_Electronic_tax_declaration_log.png)

## <a name="preview-the-xml-file"></a><span data-ttu-id="becc7-349">Vorschau der XML-Datei</span><span class="sxs-lookup"><span data-stu-id="becc7-349">Preview the XML file</span></span>

1. <span data-ttu-id="becc7-350">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**.</span><span class="sxs-lookup"><span data-stu-id="becc7-350">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**.</span></span>
2. <span data-ttu-id="becc7-351">Auf der Seite **Protokoll der elektronischen Steuererklärung**, wählen Sie die **Vorschau**-Registerkarte, um eine Vorschau der gemeldeten Werte anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="becc7-351">On the **Electronic tax declaration log** page, select the **Preview** tab to preview the reported values.</span></span>
3. <span data-ttu-id="becc7-352">Um die XML-Datei zur weiteren Übermittlung (außerhalb des Systems) zu überprüfen oder zu speichern, wählen Sie die Zeile auf der **Protokoll der elektronischen Steuererklärung**-Seite, und wählen Sie dann das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="becc7-352">To review or save the XML file for further submission (outside of the system), select the line on the **Electronic tax declaration log** page, and then select the paper clip symbol in the upper-right corner.</span></span>
4. <span data-ttu-id="becc7-353">Die **Handhabung von Dokumenten**-Seite erscheint und zeigt die generierte Datei.</span><span class="sxs-lookup"><span data-stu-id="becc7-353">The **Document handling** page appears and shows the generated file.</span></span> <span data-ttu-id="becc7-354">Wählen Sie **Öffnen** oben auf der Seite, um die Datei in der Anwendung zu öffnen, die der XML-Erweiterung in Ihrem System zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="becc7-354">Select **Open** at the top of the page to open the file in the application that is associated with the .xml extension in your system.</span></span>

## <a name="submission-the-vat-declaration-to-elster"></a><span data-ttu-id="becc7-355">Senden Sie die Umsatzsteuererklärung an ELSTER</span><span class="sxs-lookup"><span data-stu-id="becc7-355">Submission the VAT declaration to ELSTER</span></span>

<span data-ttu-id="becc7-356">ELSTER (Elektronische Steuererklärung) ist ein deutsches Online-Finanzamt, das vom Bundeszentralen Finanzamt für die Online-Einreichung von Steuererklärungen konzipiert wurde.</span><span class="sxs-lookup"><span data-stu-id="becc7-356">ELSTER (Elektronische Steuererklärung, or electronic tax declaration) is a German online tax office system that was designed by the Federal Central Tax Office for online submission of tax declarations.</span></span>

<span data-ttu-id="becc7-357">Im [Entwicklerbereich](https://www.elster.de/elsterweb/entwickler/infoseite/download_eric_28.) auf der ELSTER-Website finden Sie Beispiele, die zeigen, wie Entwickler mit ELSTER Rich Client (ERiC) interagieren können, um Mehrwertsteuererklärungen im XML-Dateiformat einzureichen.</span><span class="sxs-lookup"><span data-stu-id="becc7-357">The [Developers area](https://www.elster.de/elsterweb/entwickler/infoseite/download_eric_28.) of the ELSTER website provides examples that show how developers can interact with ELSTER Rich Client (ERiC) for the submission of VAT declarations in XML file format.</span></span> <span data-ttu-id="becc7-358">Beispiele werden für C++, C\# und Java bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="becc7-358">Examples are provided for C++, C\#, and Java.</span></span> <span data-ttu-id="becc7-359">Um auf diesen Bereich der Website zugreifen zu können, müssen Sie [als Entwickler registriert](https://www.elster.de/elsterweb/registrierung-entwickler) sein.</span><span class="sxs-lookup"><span data-stu-id="becc7-359">To access this area of the website, you must be [registered as a developer](https://www.elster.de/elsterweb/registrierung-entwickler).</span></span> <span data-ttu-id="becc7-360">Ein Beispiel könnte Ihnen helfen, Ihre eigene ausführbare Datei zu erstellen, mit der Sie XML-Dateien über ERiC senden können.</span><span class="sxs-lookup"><span data-stu-id="becc7-360">An example might help you create your own executable file that you can use to submit XML files via ERiC.</span></span> <span data-ttu-id="becc7-361">Um eine ausführbare Datei zum Senden von XML-Dateien an ELSTER zu verwenden, müssen Sie ERiC Dynamics Link Libraries (DLLs) herunterladen.</span><span class="sxs-lookup"><span data-stu-id="becc7-361">To use an executable file to submit XML files to ELSTER, you must download ERiC dynamics-link libraries (DLLs).</span></span>

<span data-ttu-id="becc7-362">Weitere Informationen zu ERiC-Versionen finden Sie unter [ELSTER-Website](https://www.elster.de/elsterweb/entwickler/infoseite/eric).</span><span class="sxs-lookup"><span data-stu-id="becc7-362">For more information about ERiC releases, see [ELSTER website](https://www.elster.de/elsterweb/entwickler/infoseite/eric).</span></span>

## <a name="example"></a><a name="example"></a> <span data-ttu-id="becc7-363">Beispiel</span><span class="sxs-lookup"><span data-stu-id="becc7-363">Example</span></span>

<span data-ttu-id="becc7-364">Das folgende Beispiel zeigt, wie Sie Umsatzsteuerkennzeichen und Umsatzsteuerberichtscodes einrichten, Transaktionen buchen und die deutsche Umsatzsteuererklärung erstellen können.</span><span class="sxs-lookup"><span data-stu-id="becc7-364">The following example shows how you can set up sales tax codes and sales tax reporting codes, post transactions, and generate the German VAT declaration.</span></span>

1. <span data-ttu-id="becc7-365">Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuercodes** und richten Sie die folgenden Umsatzsteuerkennzeichen ein.</span><span class="sxs-lookup"><span data-stu-id="becc7-365">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**, and set up the following sales tax codes.</span></span>

| <span data-ttu-id="becc7-366">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="becc7-366">**Sales tax code**</span></span> | <span data-ttu-id="becc7-367">**Prozentsatz**</span><span class="sxs-lookup"><span data-stu-id="becc7-367">**Percentage**</span></span> | <span data-ttu-id="becc7-368">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="becc7-368">**Description**</span></span>                                                                       |
|--------------------|----------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="becc7-369">VAT19</span><span class="sxs-lookup"><span data-stu-id="becc7-369">VAT19</span></span>              | <span data-ttu-id="becc7-370">19</span><span class="sxs-lookup"><span data-stu-id="becc7-370">19</span></span>             | <span data-ttu-id="becc7-371">Inlandsverkäufe mit einer Quote von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="becc7-371">Domestic sales at a rate of 19 percent.</span></span>                                               |
| <span data-ttu-id="becc7-372">VAT7</span><span class="sxs-lookup"><span data-stu-id="becc7-372">VAT7</span></span>               | <span data-ttu-id="becc7-373">7</span><span class="sxs-lookup"><span data-stu-id="becc7-373">7</span></span>              | <span data-ttu-id="becc7-374">Inlandsverkäufe mit einer Quote von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="becc7-374">Domestic sales at a rate of 7 percent.</span></span>                                                |
| <span data-ttu-id="becc7-375">InVAT19</span><span class="sxs-lookup"><span data-stu-id="becc7-375">InVAT19</span></span>            | <span data-ttu-id="becc7-376">19</span><span class="sxs-lookup"><span data-stu-id="becc7-376">19</span></span>             | <span data-ttu-id="becc7-377">Inlandseinkäufe mit einer Quote von 19 Prozent.</span><span class="sxs-lookup"><span data-stu-id="becc7-377">Domestic purchases at a rate of 19 percent.</span></span>                                           |
| <span data-ttu-id="becc7-378">InVAT7</span><span class="sxs-lookup"><span data-stu-id="becc7-378">InVAT7</span></span>             | <span data-ttu-id="becc7-379">7</span><span class="sxs-lookup"><span data-stu-id="becc7-379">7</span></span>              | <span data-ttu-id="becc7-380">Inlandseinkäufe mit einer Quote von 7 Prozent.</span><span class="sxs-lookup"><span data-stu-id="becc7-380">Domestic purchases at a rate of 7 percent.</span></span>                                            |
| <span data-ttu-id="becc7-381">EU19</span><span class="sxs-lookup"><span data-stu-id="becc7-381">EU19</span></span>               | <span data-ttu-id="becc7-382">19</span><span class="sxs-lookup"><span data-stu-id="becc7-382">19</span></span>             | <span data-ttu-id="becc7-383">EU-Einkäufe mit einer Quote von 19 Prozent, wobei die **Erwerbsteuer (USA)**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="becc7-383">EU purchases at a rate of 19 percent, where the **Use tax** option is set to **Yes**.</span></span> |
| <span data-ttu-id="becc7-384">EU7</span><span class="sxs-lookup"><span data-stu-id="becc7-384">EU7</span></span>                | <span data-ttu-id="becc7-385">7</span><span class="sxs-lookup"><span data-stu-id="becc7-385">7</span></span>              | <span data-ttu-id="becc7-386">EU-Einkäufe mit einer Quote von 7 Prozent, wobei die **Erwerbsteuer (USA)**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="becc7-386">EU purchases at a rate of 7 percent, where the **Use tax** option is set to **Yes**.</span></span>  |
| <span data-ttu-id="becc7-387">EUS</span><span class="sxs-lookup"><span data-stu-id="becc7-387">EUS</span></span>                | <span data-ttu-id="becc7-388">19</span><span class="sxs-lookup"><span data-stu-id="becc7-388">19</span></span>             | <span data-ttu-id="becc7-389">EU-Verkäufe, bei denen die **Befreit**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="becc7-389">EU sales where the **Exempt** option is set to **Yes**.</span></span>                               |
| <span data-ttu-id="becc7-390">THIRD</span><span class="sxs-lookup"><span data-stu-id="becc7-390">THIRD</span></span>              | <span data-ttu-id="becc7-391">19</span><span class="sxs-lookup"><span data-stu-id="becc7-391">19</span></span>             | <span data-ttu-id="becc7-392">Exportverkäufe, bei denen die **Befreit**-Option auf **Ja** gesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="becc7-392">Export sales where the **Exempt** option is set to **Yes**.</span></span>                           |

2. <span data-ttu-id="becc7-393">Auf der **Mehrwertsteuercodes**-Seite weisen Sie auf dem Inforegister **Berichtseinstellungen** den Mehrwertsteuercodes Berichtscodes zu.</span><span class="sxs-lookup"><span data-stu-id="becc7-393">On the **Sales tax codes** page, on the **Report setup** FastTab, assign reporting codes to sales tax codes.</span></span>

<span data-ttu-id="becc7-394">Die folgende Tabelle zeigt, wie Sie die Mehrwertsteuer-Berichtscodes den Mehrwertsteuercodes zuweisen.</span><span class="sxs-lookup"><span data-stu-id="becc7-394">The following table shows how to assign the sales tax reporting codes to sales tax codes.</span></span>

| <span data-ttu-id="becc7-395">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="becc7-395">**Sales tax code**</span></span> | <span data-ttu-id="becc7-396">**Steuerpflichtiger Umsatz**</span><span class="sxs-lookup"><span data-stu-id="becc7-396">**Taxable sales**</span></span> | <span data-ttu-id="becc7-397">**Steuerfreier Verkauf**</span><span class="sxs-lookup"><span data-stu-id="becc7-397">**Tax-free sale**</span></span> | <span data-ttu-id="becc7-398">**Mehrwertsteuer**</span><span class="sxs-lookup"><span data-stu-id="becc7-398">**Sales tax payable**</span></span> | <span data-ttu-id="becc7-399">**Steuerpflichtige Einkäufe**</span><span class="sxs-lookup"><span data-stu-id="becc7-399">**Taxable purchases**</span></span> | <span data-ttu-id="becc7-400">**Vorsteuer**</span><span class="sxs-lookup"><span data-stu-id="becc7-400">**Sales tax receivable**</span></span> | <span data-ttu-id="becc7-401">**Steuerpflichtiger Import**</span><span class="sxs-lookup"><span data-stu-id="becc7-401">**Taxable import**</span></span> | <span data-ttu-id="becc7-402">**Erwerbsteuer (USA)**</span><span class="sxs-lookup"><span data-stu-id="becc7-402">**Use tax**</span></span> | <span data-ttu-id="becc7-403">**Erwerbsteuerausgleich**</span><span class="sxs-lookup"><span data-stu-id="becc7-403">**Offset use tax**</span></span> |
|--------------------|-------------------|-------------------|-----------------------|-----------------------|--------------------------|--------------------|-------------|--------------------|
| <span data-ttu-id="becc7-404">VAT19</span><span class="sxs-lookup"><span data-stu-id="becc7-404">VAT19</span></span>              | <span data-ttu-id="becc7-405">81</span><span class="sxs-lookup"><span data-stu-id="becc7-405">81</span></span>                |                   | <span data-ttu-id="becc7-406">181</span><span class="sxs-lookup"><span data-stu-id="becc7-406">181</span></span>                   |                       |                          |                    |             |                    |
| <span data-ttu-id="becc7-407">VAT7</span><span class="sxs-lookup"><span data-stu-id="becc7-407">VAT7</span></span>               | <span data-ttu-id="becc7-408">86</span><span class="sxs-lookup"><span data-stu-id="becc7-408">86</span></span>                |                   | <span data-ttu-id="becc7-409">186</span><span class="sxs-lookup"><span data-stu-id="becc7-409">186</span></span>                   |                       |                          |                    |             |                    |
| <span data-ttu-id="becc7-410">InVAT19</span><span class="sxs-lookup"><span data-stu-id="becc7-410">InVAT19</span></span>            |                   |                   |                       |                       | <span data-ttu-id="becc7-411">66</span><span class="sxs-lookup"><span data-stu-id="becc7-411">66</span></span>                       |                    |             |                    |
| <span data-ttu-id="becc7-412">InVAT7</span><span class="sxs-lookup"><span data-stu-id="becc7-412">InVAT7</span></span>             |                   |                   |                       |                       | <span data-ttu-id="becc7-413">66</span><span class="sxs-lookup"><span data-stu-id="becc7-413">66</span></span>                       |                    |             |                    |
| <span data-ttu-id="becc7-414">EU19</span><span class="sxs-lookup"><span data-stu-id="becc7-414">EU19</span></span>               |                   |                   |                       |                       |                          | <span data-ttu-id="becc7-415">89</span><span class="sxs-lookup"><span data-stu-id="becc7-415">89</span></span>                 | <span data-ttu-id="becc7-416">189</span><span class="sxs-lookup"><span data-stu-id="becc7-416">189</span></span>         | <span data-ttu-id="becc7-417">61</span><span class="sxs-lookup"><span data-stu-id="becc7-417">61</span></span>                 |
| <span data-ttu-id="becc7-418">EU7</span><span class="sxs-lookup"><span data-stu-id="becc7-418">EU7</span></span>                |                   |                   |                       |                       |                          | <span data-ttu-id="becc7-419">93</span><span class="sxs-lookup"><span data-stu-id="becc7-419">93</span></span>                 | <span data-ttu-id="becc7-420">193</span><span class="sxs-lookup"><span data-stu-id="becc7-420">193</span></span>         | <span data-ttu-id="becc7-421">61</span><span class="sxs-lookup"><span data-stu-id="becc7-421">61</span></span>                 |
| <span data-ttu-id="becc7-422">EUS</span><span class="sxs-lookup"><span data-stu-id="becc7-422">EUS</span></span>                |                   | <span data-ttu-id="becc7-423">41</span><span class="sxs-lookup"><span data-stu-id="becc7-423">41</span></span>                |                       |                       |                          |                    |             |                    |
| <span data-ttu-id="becc7-424">THIRD</span><span class="sxs-lookup"><span data-stu-id="becc7-424">THIRD</span></span>              |                   | <span data-ttu-id="becc7-425">43</span><span class="sxs-lookup"><span data-stu-id="becc7-425">43</span></span>                |                       |                       |                          |                    |             |                    |

> [!NOTE]
> <span data-ttu-id="becc7-426">Die vorhergehende Konfiguration ist nur ein Beispiel und hängt von der Struktur der Mehrwertsteuercodes ab, die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="becc7-426">The preceding configuration is just an example and depends on the structure of the sales tax codes that are used.</span></span> <span data-ttu-id="becc7-427">Damit Werte für die Mehrwertsteuererklärung berechnet und übertragen werde, müssen Sie für jeden Steuercode, der im Mehrwertsteuerzahlungsprozess verwendet wird, einen entsprechenden Mehrwertsteuer-Erklärungscode in einem oder mehreren Feldern der Registerkarte **Berichteinstellung** festlegen.</span><span class="sxs-lookup"><span data-stu-id="becc7-427">If you want values to be calculated and transferred to the sales tax report, for each tax code that is used in the sales tax payment process, you must set a relevant sales tax reporting code in one or more fields on the **Report setup** FastTab.</span></span>

3. <span data-ttu-id="becc7-428">Wechseln Sie zu **Steuer \> Einstellung \> Mehrwertsteuer \> Einrichtung der elektronischen Steuererklärung**.</span><span class="sxs-lookup"><span data-stu-id="becc7-428">Go to **Tax \> Setup \> Sales tax \> Electronic tax declaration setup**.</span></span>
4. <span data-ttu-id="becc7-429">Im Feld **Formatzuordnung** wählen Sie das Format **Elster (DE)** aus, das Sie zuvor heruntergeladen haben.</span><span class="sxs-lookup"><span data-stu-id="becc7-429">In the **Format mapping** field, select the **Elster (DE)** format that you downloaded earlier.</span></span>
5. <span data-ttu-id="becc7-430">Führen Sie die folgenden Buchungen aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-430">Post the following transactions.</span></span> <span data-ttu-id="becc7-431">Informationen zu Kundenrechnungen finden Sie beispielsweise unter **Debitorenkonten** \> **Rechnungen** \> **Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="becc7-431">For example, for customer invoices, go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span> <span data-ttu-id="becc7-432">Kreditorenrechnungen wechseln Sie zu **Kreditorenkonten \> Rechnungen \> Rechnungserfassung**.</span><span class="sxs-lookup"><span data-stu-id="becc7-432">For vendor invoices, go to **Accounts payable \> Invoices \> Invoice journal**.</span></span>

| <span data-ttu-id="becc7-433">**Datum**</span><span class="sxs-lookup"><span data-stu-id="becc7-433">**Date**</span></span>        | <span data-ttu-id="becc7-434">**Buchungstyp**</span><span class="sxs-lookup"><span data-stu-id="becc7-434">**Transaction type**</span></span>      | <span data-ttu-id="becc7-435">**Nettobetrag**</span><span class="sxs-lookup"><span data-stu-id="becc7-435">**Amount net**</span></span> | <span data-ttu-id="becc7-436">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="becc7-436">**VAT amount**</span></span> | <span data-ttu-id="becc7-437">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="becc7-437">**Sales tax code**</span></span> | <span data-ttu-id="becc7-438">**Erwartete Steuerbemessungsgrundlage – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="becc7-438">**Expected tax base – reporting code**</span></span> | <span data-ttu-id="becc7-439">**Erwarteter Steuerbemessungsbetrag – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="becc7-439">**Expected tax amount – reporting code**</span></span> |
|-----------------|---------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| <span data-ttu-id="becc7-440">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="becc7-440">January 1, 2020</span></span> | <span data-ttu-id="becc7-441">Debitorenrechnung</span><span class="sxs-lookup"><span data-stu-id="becc7-441">Customer invoice</span></span>          | <span data-ttu-id="becc7-442">100</span><span class="sxs-lookup"><span data-stu-id="becc7-442">100</span></span>            | <span data-ttu-id="becc7-443">19</span><span class="sxs-lookup"><span data-stu-id="becc7-443">19</span></span>             | <span data-ttu-id="becc7-444">VAT19</span><span class="sxs-lookup"><span data-stu-id="becc7-444">VAT19</span></span>              | <span data-ttu-id="becc7-445">81</span><span class="sxs-lookup"><span data-stu-id="becc7-445">81</span></span>                                     | <span data-ttu-id="becc7-446">181</span><span class="sxs-lookup"><span data-stu-id="becc7-446">181</span></span>                                      |
| <span data-ttu-id="becc7-447">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="becc7-447">January 1, 2020</span></span> | <span data-ttu-id="becc7-448">Kreditorenrechnung (EU)</span><span class="sxs-lookup"><span data-stu-id="becc7-448">Vendor invoice (EU)</span></span>       | <span data-ttu-id="becc7-449">100</span><span class="sxs-lookup"><span data-stu-id="becc7-449">100</span></span>            | <span data-ttu-id="becc7-450">7</span><span class="sxs-lookup"><span data-stu-id="becc7-450">7</span></span>              | <span data-ttu-id="becc7-451">EU7</span><span class="sxs-lookup"><span data-stu-id="becc7-451">EU7</span></span>                | <span data-ttu-id="becc7-452">93</span><span class="sxs-lookup"><span data-stu-id="becc7-452">93</span></span>                                     | <span data-ttu-id="becc7-453">193 – Steuerpflichtig 61 – Steuerabzug</span><span class="sxs-lookup"><span data-stu-id="becc7-453">193 – Tax payable 61 – Tax deduction</span></span>     |
| <span data-ttu-id="becc7-454">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="becc7-454">January 1, 2020</span></span> | <span data-ttu-id="becc7-455">Debitorenrechnung (EU)</span><span class="sxs-lookup"><span data-stu-id="becc7-455">Customer invoice (EU)</span></span>     | <span data-ttu-id="becc7-456">100</span><span class="sxs-lookup"><span data-stu-id="becc7-456">100</span></span>            | <span data-ttu-id="becc7-457">0</span><span class="sxs-lookup"><span data-stu-id="becc7-457">0</span></span>              | <span data-ttu-id="becc7-458">EUS</span><span class="sxs-lookup"><span data-stu-id="becc7-458">EUS</span></span>                | <span data-ttu-id="becc7-459">41</span><span class="sxs-lookup"><span data-stu-id="becc7-459">41</span></span>                                     | <span data-ttu-id="becc7-460">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="becc7-460">Not applicable</span></span>                           |
| <span data-ttu-id="becc7-461">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="becc7-461">January 1, 2020</span></span> | <span data-ttu-id="becc7-462">Debitorenrechnung (Export)</span><span class="sxs-lookup"><span data-stu-id="becc7-462">Customer invoice (export)</span></span> | <span data-ttu-id="becc7-463">100</span><span class="sxs-lookup"><span data-stu-id="becc7-463">100</span></span>            | <span data-ttu-id="becc7-464">0</span><span class="sxs-lookup"><span data-stu-id="becc7-464">0</span></span>              | <span data-ttu-id="becc7-465">THIRD</span><span class="sxs-lookup"><span data-stu-id="becc7-465">THIRD</span></span>              | <span data-ttu-id="becc7-466">43</span><span class="sxs-lookup"><span data-stu-id="becc7-466">43</span></span>                                     | <span data-ttu-id="becc7-467">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="becc7-467">Not applicable</span></span>                           |

6. <span data-ttu-id="becc7-468">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="becc7-468">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
7. <span data-ttu-id="becc7-469">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder auf die angegebenen Werte ein.</span><span class="sxs-lookup"><span data-stu-id="becc7-469">In the **Report sales tax for settlement period** dialog box, set the following fields to the specified values:</span></span>

    - <span data-ttu-id="becc7-470">**Ausgleichsperiode:** Mo</span><span class="sxs-lookup"><span data-stu-id="becc7-470">**Settlement period:** Mon</span></span>
    - <span data-ttu-id="becc7-471">**Von Datum** = 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="becc7-471">**From date:** 1/1/2020</span></span>

8. <span data-ttu-id="becc7-472">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-472">Select **OK**.</span></span>
9. <span data-ttu-id="becc7-473">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld wählen Sie das **Elektronisches Steuerdokument erstellen**-Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="becc7-473">In the **German sales tax report** dialog box, select the **Create electronic tax document** check box.</span></span>
10. <span data-ttu-id="becc7-474">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-474">Select **OK**.</span></span>
11. <span data-ttu-id="becc7-475">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**, und wählen Sie die erforderliche Position aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-475">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**, and select the required line.</span></span>
12. <span data-ttu-id="becc7-476">Auf der **Protokoll der elektronischen Steuererklärung**-Seite, wählen Sie die **Allgemein**-Registerkarte und überprüfen die allgemeinen Informationen.</span><span class="sxs-lookup"><span data-stu-id="becc7-476">On the **Electronic tax declaration log** page, select the **General** tab, and review the general information.</span></span>

![Seite „Protokoll der elektronischen Steuererklärung“, Registerkarte „Allgemein“](media/2_Electronic_tax_declaration_log.png)

13. <span data-ttu-id="becc7-478">Wählen Sie **Vorschau** aus, klicken Sie auf die Registerkarte und überprüfen Sie die gemeldeten Werte.</span><span class="sxs-lookup"><span data-stu-id="becc7-478">Select the **Preview** tab, and review the reported values.</span></span>

![Vorschau des Protokolls der elektronischen Steuererklärung](media/3_Electronic_tax_declaration_log.png)

14. <span data-ttu-id="becc7-480">Wählen Sie das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="becc7-480">Select the paper clip symbol in the upper-right corner.</span></span>
15. <span data-ttu-id="becc7-481">Wählen Sie **Öffnen** und überprüfen Sie die XML-Datei oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="becc7-481">Select **Open** at the top of the page, and review the XML file.</span></span>

![XML-Datei](media/4_XML_file.png)

### <a name="correction-transactions"></a><span data-ttu-id="becc7-483">Korrekturtransaktionen</span><span class="sxs-lookup"><span data-stu-id="becc7-483">Correction transactions</span></span>

1.  <span data-ttu-id="becc7-484">Wählen Sie eine neue Transaktion aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-484">Post a new transaction.</span></span> <span data-ttu-id="becc7-485">Informationen zur Buchung einer Kundenrechnung finden Sie beispielsweise unter **Debitorenkonten** \> **Rechnungen** \> **Alle Freitextrechnungen**.</span><span class="sxs-lookup"><span data-stu-id="becc7-485">For example, to post a customer invoice, go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>

| <span data-ttu-id="becc7-486">**Datum**</span><span class="sxs-lookup"><span data-stu-id="becc7-486">**Date**</span></span>        | <span data-ttu-id="becc7-487">**Buchungstyp**</span><span class="sxs-lookup"><span data-stu-id="becc7-487">**Transaction type**</span></span>        | <span data-ttu-id="becc7-488">**Nettobetrag**</span><span class="sxs-lookup"><span data-stu-id="becc7-488">**Amount net**</span></span> | <span data-ttu-id="becc7-489">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="becc7-489">**VAT amount**</span></span> | <span data-ttu-id="becc7-490">**Mehrwertsteuercode**</span><span class="sxs-lookup"><span data-stu-id="becc7-490">**Sales tax code**</span></span> | <span data-ttu-id="becc7-491">**Erwartete Steuerbemessungsgrundlage – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="becc7-491">**Expected tax base – Reporting code**</span></span> | <span data-ttu-id="becc7-492">**Erwarteter Steuerbemessungsbetrag – Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="becc7-492">**Expected tax amount – Reporting code**</span></span> |
|-----------------|-----------------------------|----------------|----------------|--------------------|----------------------------------------|------------------------------------------|
| <span data-ttu-id="becc7-493">1. Januar 2020</span><span class="sxs-lookup"><span data-stu-id="becc7-493">January 1, 2020</span></span> | <span data-ttu-id="becc7-494">Debitorenrechnung (Inland)</span><span class="sxs-lookup"><span data-stu-id="becc7-494">Customer invoice (domestic)</span></span> | <span data-ttu-id="becc7-495">100</span><span class="sxs-lookup"><span data-stu-id="becc7-495">100</span></span>            | <span data-ttu-id="becc7-496">7</span><span class="sxs-lookup"><span data-stu-id="becc7-496">7</span></span>              | <span data-ttu-id="becc7-497">VAT7</span><span class="sxs-lookup"><span data-stu-id="becc7-497">VAT7</span></span>               | <span data-ttu-id="becc7-498">86</span><span class="sxs-lookup"><span data-stu-id="becc7-498">86</span></span>                                     | <span data-ttu-id="becc7-499">186</span><span class="sxs-lookup"><span data-stu-id="becc7-499">186</span></span>                                      |

2. <span data-ttu-id="becc7-500">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="becc7-500">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
3. <span data-ttu-id="becc7-501">Im Dialogfeld **Umsatzsteuer für Abrechnungszeitraum melden** stellen Sie die folgenden Felder auf die angegebenen Werte ein.</span><span class="sxs-lookup"><span data-stu-id="becc7-501">In the **Report sales tax for settlement period** dialog box, set the following fields to the specified values:</span></span>

    - <span data-ttu-id="becc7-502">**Ausgleichsperiode:** Mo</span><span class="sxs-lookup"><span data-stu-id="becc7-502">**Settlement period:** Mon</span></span>
    - <span data-ttu-id="becc7-503">**Von Datum** = 1/1/2020</span><span class="sxs-lookup"><span data-stu-id="becc7-503">**From date:** 1/1/2020</span></span>

4. <span data-ttu-id="becc7-504">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-504">Select **OK**.</span></span>
5. <span data-ttu-id="becc7-505">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld wählen Sie das **Elektronisches Steuerdokument erstellen**-Kontrollkästchen.</span><span class="sxs-lookup"><span data-stu-id="becc7-505">In the **German sales tax report** dialog box, select the **Create electronic tax document** check box.</span></span>
6. <span data-ttu-id="becc7-506">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-506">Select **OK**.</span></span>
7. <span data-ttu-id="becc7-507">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Protokoll der elektronischen Steuererklärung**, und wählen Sie die erforderliche Position aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-507">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Electronic tax declaration log**, and select the required line.</span></span>
8. <span data-ttu-id="becc7-508">Wählen Sie **Vorschau** aus, klicken Sie auf die Registerkarte und überprüfen Sie die gemeldeten Werte.</span><span class="sxs-lookup"><span data-stu-id="becc7-508">Select the **Preview** tab, and review the reported values.</span></span>

![Vorschau des Protokolls der elektronischen Steuererklärung](media/5_Electronic_tax_declaration_log.png)

<span data-ttu-id="becc7-510">Beachten Sie, dass eine Korrekturtransaktion zur Erklärung in Codes **86** und **83** hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="becc7-510">Note that a correction transaction is added to the declaration in codes **86** and **83**.</span></span>

9. <span data-ttu-id="becc7-511">Wählen Sie das Büroklammersymbol in der oberen rechten Ecke.</span><span class="sxs-lookup"><span data-stu-id="becc7-511">Select the paper clip symbol in the upper-right corner.</span></span>
10. <span data-ttu-id="becc7-512">Wählen Sie **Öffnen** und überprüfen Sie die XML-Datei oben auf der Seite.</span><span class="sxs-lookup"><span data-stu-id="becc7-512">Select **Open** at the top of the page, and review the XML file.</span></span>

![XML-Datei](media/6_XML_file.png)

<span data-ttu-id="becc7-514">Beachten Sie, dass eine Korrekturtransaktion zur Erklärung in Codes **86** und **83** hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="becc7-514">Note that a correction transaction is added to the declaration in codes **86** and **83**.</span></span>

## <a name="review-sales-tax-report-amounts"></a><span data-ttu-id="becc7-515">Überprüfen Sie die Beträge des Umsatzsteuerberichts</span><span class="sxs-lookup"><span data-stu-id="becc7-515">Review sales tax report amounts</span></span> 

<span data-ttu-id="becc7-516">Sie können den Umsatzsteuerbetrag optional im SSRS-Bericht überprüfen.</span><span class="sxs-lookup"><span data-stu-id="becc7-516">You can optionally review sales tax amount in SSRS report.</span></span>

### <a name="set-up-the-report-layout-for-sales-tax-authorities"></a><span data-ttu-id="becc7-517">Richten Sie das Berichtslayout für die Umsatzsteuerbehörden ein</span><span class="sxs-lookup"><span data-stu-id="becc7-517">Set up the report layout for sales tax authorities</span></span>

1. <span data-ttu-id="becc7-518">Wechseln Sie zu **Steuer** \> **Indirekte Steuern** \> **Mehrwertsteuer** \> **Mehrwertsteuerbehörden**.</span><span class="sxs-lookup"><span data-stu-id="becc7-518">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax authorities**.</span></span>
2. <span data-ttu-id="becc7-519">Wählen Sie auf der Seite **Mehrwertsteuer-Behörden** die Mehrwertsteuerbehörde, die für den Mehrwertsteuer-Abrechnungszeitraum in den Mehrwertsteuercodes verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="becc7-519">On the **Sales tax authorities** page, select the sales tax authority that will be used in the sales tax codes for the sales tax settlement period.</span></span>
3. <span data-ttu-id="becc7-520">Im **Berichtslayout**-Feld wählen Sie **Deutsches Steuererklärungslayout**.</span><span class="sxs-lookup"><span data-stu-id="becc7-520">In the **Report layout** field, select **German report layout**.</span></span>

### <a name="generate-a-sales-tax-payment-and-print-the-german-sales-tax-report"></a><a name="generatesalestaxpayment"></a> <span data-ttu-id="becc7-521">Generieren Sie eine Mehrwertsteuerzahlung und drucken Sie den deutschen Mehrwertsteuerbericht aus</span><span class="sxs-lookup"><span data-stu-id="becc7-521">Generate a sales tax payment and print the German sales tax report</span></span>

<span data-ttu-id="becc7-522">Berechnen Sie am Ende des MwSt.-Berichtszeitraums die Mehrwertsteuerbeträge für den Abrechnungszeitraum.</span><span class="sxs-lookup"><span data-stu-id="becc7-522">At the end of the VAT reporting period, calculate the sales tax amounts for the settlement period.</span></span>

1. <span data-ttu-id="becc7-523">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="becc7-523">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
2. <span data-ttu-id="becc7-524">Im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld stellen die erforderlichen Felder wie [vorhin](#createvatdecxmlformat) beschrieben ein.</span><span class="sxs-lookup"><span data-stu-id="becc7-524">In the **Settle and post sales tax** dialog box, set the required fields as described [earlier](#createvatdecxmlformat).</span></span>
3. <span data-ttu-id="becc7-525">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-525">Select **OK**.</span></span>
4. <span data-ttu-id="becc7-526">Im **Deutsche Mehrwertsteuererklärung**-Dialogfeld legen Sie die **Elektronisches Steuerdokument erstellen**-Option auf **Nein** fest.</span><span class="sxs-lookup"><span data-stu-id="becc7-526">In the **German sales tax report** dialog box, set the **Create electronic tax document** option to **No**.</span></span>
5. <span data-ttu-id="becc7-527">Wählen Sie **OK** aus, um die Mehrwertsteuerzahlung zu generieren und den Bericht zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="becc7-527">Select **OK** to generate the sales tax payment and review the report.</span></span>

<span data-ttu-id="becc7-528">Wenn Sie Transaktionen wie in Schritt 5 des [Beispiels](#example) zu Beginn dieses Themas buchen, werden die folgenden Daten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="becc7-528">If you post transactions as described in step 5 of the [example](#example) earlier in this topic, you will see the following data.</span></span>

![Generierter deutscher Mehrwertsteuerbericht, Seite 1](media/7_Sales_tax_reporting.png)

![Generierter deutscher Mehrwertsteuerbericht, Seite 2](media/8_Sales_tax_reporting.png)

### <a name="print-a-sales-tax-payment-report-from-a-sales-tax-payment"></a><span data-ttu-id="becc7-531">Drucken Sie einen Mehrwertsteuerzahlungsbericht aus einer Mehrwertsteuerzahlung</span><span class="sxs-lookup"><span data-stu-id="becc7-531">Print a sales tax payment report from a sales tax payment</span></span>

1. <span data-ttu-id="becc7-532">Wechseln Sie zu **Steuer** \> **Anfragen und Berichte** \> **Mehrwertsteuerzahlungen**.</span><span class="sxs-lookup"><span data-stu-id="becc7-532">Go to **Tax** \> **Inquiries and reports** \> **Sales tax payments**.</span></span>
2. <span data-ttu-id="becc7-533">Auf der **Mehrwertsteuerzahlung**-Seite wählen Sie den Datensatz aus und wählen dann **Bericht drucken** aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-533">On the **Sales tax payment** page, select the record, and then select **Print report**.</span></span>
3. <span data-ttu-id="becc7-534">Stellen Sie im Dialogfeld die Felder wie im vorherigen Abschnitt beschrieben ein und wählen Sie dann **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-534">In the dialog box, set the fields as described in the previous section, and then select **OK**.</span></span>

### <a name="report-sales-tax-for-the-settlement-period"></a><span data-ttu-id="becc7-535">Umsatzsteuer für Abrechnungszeitraum melden</span><span class="sxs-lookup"><span data-stu-id="becc7-535">Report sales tax for the settlement period</span></span>

<span data-ttu-id="becc7-536">Sie können den deutschen Mehrwertsteuerbericht auch mit der **Umsatzsteuer für Abrechnungszeitraum melden**-Anfrage erstellen.</span><span class="sxs-lookup"><span data-stu-id="becc7-536">You can also generate the German sales tax report by using the **Report sales tax for settlement period** inquiry.</span></span>

1. <span data-ttu-id="becc7-537">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="becc7-537">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
2. <span data-ttu-id="becc7-538">Im **Umsatzsteuer für Abrechnungszeitraum melden**-Dialogfeld, stellen Sie die **Ausgleichsperiode** und die **Anfangsdatum**-Felder wie im Abschnitt [Generieren Sie eine Mehrwertsteuerzahlung und drucken Sie den deutschen Mehrwertsteuerbericht aus](#generatesalestaxpayment) weiter oben in diesem Thema beschrieben ein.</span><span class="sxs-lookup"><span data-stu-id="becc7-538">In the **Report sales tax for settlement period** dialog box, set the **Settlement period** and **From date** fields as described in the [Generate a sales tax payment and print the German sales tax report](#generatesalestaxpayment) section earlier in this topic.</span></span>
3. <span data-ttu-id="becc7-539">Wählen Sie im Feld **Mehrwertsteuer, Zahlungsversion** einen der folgenden Werte aus:</span><span class="sxs-lookup"><span data-stu-id="becc7-539">In the **Sales tax payment version** field, select one of the following values:</span></span>

- <span data-ttu-id="becc7-540">**Original** – Einen Mehrwertsteuerbericht generieren für die erste gebuchte Ausgleichsberechnung für das Periodenintervall.</span><span class="sxs-lookup"><span data-stu-id="becc7-540">**Original** – Generate a report for sales tax transactions of the first posted settlement calculation for the period.</span></span>
- <span data-ttu-id="becc7-541">**Korrekturen** – Einen Mehrwertsteuerbericht generieren für nachfolgende Ausgleichsberechnungen für das Periodenintervall.</span><span class="sxs-lookup"><span data-stu-id="becc7-541">**Corrections** – Generate a report for sales tax transactions of subsequent settlement calculations for the period.</span></span>
- <span data-ttu-id="becc7-542">**Gesamtliste** – Erstellen Sie einen Bericht für alle Verkaufstransaktionen für den Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="becc7-542">**Total list** – Generate a report for all sales transactions for the period.</span></span> <span data-ttu-id="becc7-543">Diese Transaktionen umfassen ursprüngliche und korrigierte Transaktionen.</span><span class="sxs-lookup"><span data-stu-id="becc7-543">These transactions include original and corrected transactions.</span></span>

4. <span data-ttu-id="becc7-544">Wählen Sie **OK**.</span><span class="sxs-lookup"><span data-stu-id="becc7-544">Select **OK**.</span></span>
5. <span data-ttu-id="becc7-545">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="becc7-545">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
6. <span data-ttu-id="becc7-546">Wählen Sie im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Original** aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-546">In the **Settle and post sales tax** dialog box, in the **Sales tax payment version** field, select **Original**.</span></span>
7.  <span data-ttu-id="becc7-547">Drucken Sie den Bericht aus und überprüfen Sie die Daten.</span><span class="sxs-lookup"><span data-stu-id="becc7-547">Print the report, and review the data.</span></span>

| <span data-ttu-id="becc7-548">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="becc7-548">**Reporting code**</span></span> | <span data-ttu-id="becc7-549">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="becc7-549">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="becc7-550">41</span><span class="sxs-lookup"><span data-stu-id="becc7-550">41</span></span>                 | <span data-ttu-id="becc7-551">100</span><span class="sxs-lookup"><span data-stu-id="becc7-551">100</span></span>                  |
| <span data-ttu-id="becc7-552">43</span><span class="sxs-lookup"><span data-stu-id="becc7-552">43</span></span>                 | <span data-ttu-id="becc7-553">100</span><span class="sxs-lookup"><span data-stu-id="becc7-553">100</span></span>                  |
| <span data-ttu-id="becc7-554">61</span><span class="sxs-lookup"><span data-stu-id="becc7-554">61</span></span>                 | <span data-ttu-id="becc7-555">7</span><span class="sxs-lookup"><span data-stu-id="becc7-555">7</span></span>                    |
| <span data-ttu-id="becc7-556">81</span><span class="sxs-lookup"><span data-stu-id="becc7-556">81</span></span>                 | <span data-ttu-id="becc7-557">100</span><span class="sxs-lookup"><span data-stu-id="becc7-557">100</span></span>                  |
| <span data-ttu-id="becc7-558">93</span><span class="sxs-lookup"><span data-stu-id="becc7-558">93</span></span>                 | <span data-ttu-id="becc7-559">100</span><span class="sxs-lookup"><span data-stu-id="becc7-559">100</span></span>                  |
| <span data-ttu-id="becc7-560">181</span><span class="sxs-lookup"><span data-stu-id="becc7-560">181</span></span>                | <span data-ttu-id="becc7-561">19</span><span class="sxs-lookup"><span data-stu-id="becc7-561">19</span></span>                   |
| <span data-ttu-id="becc7-562">193</span><span class="sxs-lookup"><span data-stu-id="becc7-562">193</span></span>                | <span data-ttu-id="becc7-563">7</span><span class="sxs-lookup"><span data-stu-id="becc7-563">7</span></span>                    |

8. <span data-ttu-id="becc7-564">Wechseln Sie zu **Steuer** \> **Meldungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer abrechnen und buchen**.</span><span class="sxs-lookup"><span data-stu-id="becc7-564">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Settle and post sales tax**.</span></span>
9. <span data-ttu-id="becc7-565">Wählen Sie im **Mehrwertsteuer abrechnen und buchen**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Neueste Korrekturen** aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-565">In the **Settle and post sales tax** dialog box, in the **Sales tax payment version** field, select **Latest corrections**.</span></span>
10. <span data-ttu-id="becc7-566">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="becc7-566">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
11. <span data-ttu-id="becc7-567">Wählen Sie im **Mehrwertsteuer für Abrechnungszeitraum melden**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Korrekturen** aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-567">In the **Report sales tax for settlement period** dialog box, in the **Sales tax payment version** field, select **Corrections**.</span></span> <span data-ttu-id="becc7-568">Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="becc7-568">The following table shows the result.</span></span>

| <span data-ttu-id="becc7-569">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="becc7-569">**Reporting code**</span></span> | <span data-ttu-id="becc7-570">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="becc7-570">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="becc7-571">86</span><span class="sxs-lookup"><span data-stu-id="becc7-571">86</span></span>                 | <span data-ttu-id="becc7-572">100</span><span class="sxs-lookup"><span data-stu-id="becc7-572">100</span></span>                  |
| <span data-ttu-id="becc7-573">186</span><span class="sxs-lookup"><span data-stu-id="becc7-573">186</span></span>                | <span data-ttu-id="becc7-574">7</span><span class="sxs-lookup"><span data-stu-id="becc7-574">7</span></span>                    |

12. <span data-ttu-id="becc7-575">Wechseln Sie zu **Steuer** \> **Erklärungen** \> **Mehrwertsteuer** \> **Mehrwertsteuer für Abrechnungszeitraum melden**.</span><span class="sxs-lookup"><span data-stu-id="becc7-575">Go to **Tax** \> **Declarations** \> **Sales tax** \> **Report sales tax for settlement period**.</span></span>
13. <span data-ttu-id="becc7-576">Wählen Sie im **Mehrwertsteuer für Abrechnungszeitraum melden**-Dialogfeld im **Mehrwertsteuer, Zahlungsversion**-Feld **Gesamtliste** aus.</span><span class="sxs-lookup"><span data-stu-id="becc7-576">In the **Report sales tax for settlement period** dialog box, in the **Sales tax payment version** field, select **Total list**.</span></span> <span data-ttu-id="becc7-577">Die Ergebnisse werden in der folgenden Tabelle veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="becc7-577">The following table shows the result.</span></span>

| <span data-ttu-id="becc7-578">**Berichtscode**</span><span class="sxs-lookup"><span data-stu-id="becc7-578">**Reporting code**</span></span> | <span data-ttu-id="becc7-579">**Mehrwertsteuerbetrag**</span><span class="sxs-lookup"><span data-stu-id="becc7-579">**Sales tax amount**</span></span> |
|--------------------|----------------------|
| <span data-ttu-id="becc7-580">41</span><span class="sxs-lookup"><span data-stu-id="becc7-580">41</span></span>                 | <span data-ttu-id="becc7-581">100</span><span class="sxs-lookup"><span data-stu-id="becc7-581">100</span></span>                  |
| <span data-ttu-id="becc7-582">43</span><span class="sxs-lookup"><span data-stu-id="becc7-582">43</span></span>                 | <span data-ttu-id="becc7-583">100</span><span class="sxs-lookup"><span data-stu-id="becc7-583">100</span></span>                  |
| <span data-ttu-id="becc7-584">61</span><span class="sxs-lookup"><span data-stu-id="becc7-584">61</span></span>                 | <span data-ttu-id="becc7-585">7</span><span class="sxs-lookup"><span data-stu-id="becc7-585">7</span></span>                    |
| <span data-ttu-id="becc7-586">81</span><span class="sxs-lookup"><span data-stu-id="becc7-586">81</span></span>                 | <span data-ttu-id="becc7-587">100</span><span class="sxs-lookup"><span data-stu-id="becc7-587">100</span></span>                  |
| <span data-ttu-id="becc7-588">86</span><span class="sxs-lookup"><span data-stu-id="becc7-588">86</span></span>                 | <span data-ttu-id="becc7-589">100</span><span class="sxs-lookup"><span data-stu-id="becc7-589">100</span></span>                  |
| <span data-ttu-id="becc7-590">93</span><span class="sxs-lookup"><span data-stu-id="becc7-590">93</span></span>                 | <span data-ttu-id="becc7-591">100</span><span class="sxs-lookup"><span data-stu-id="becc7-591">100</span></span>                  |
| <span data-ttu-id="becc7-592">181</span><span class="sxs-lookup"><span data-stu-id="becc7-592">181</span></span>                | <span data-ttu-id="becc7-593">19</span><span class="sxs-lookup"><span data-stu-id="becc7-593">19</span></span>                   |
| <span data-ttu-id="becc7-594">186</span><span class="sxs-lookup"><span data-stu-id="becc7-594">186</span></span>                | <span data-ttu-id="becc7-595">7</span><span class="sxs-lookup"><span data-stu-id="becc7-595">7</span></span>                    |
| <span data-ttu-id="becc7-596">193</span><span class="sxs-lookup"><span data-stu-id="becc7-596">193</span></span>                | <span data-ttu-id="becc7-597">7</span><span class="sxs-lookup"><span data-stu-id="becc7-597">7</span></span>                    |
