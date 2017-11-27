---
title: "MwSt-Berichterstattung für Europa"
description: "Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung  des Mehrwertsteuer-Auszugs für einige europäische Länder."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: dd66ced17dbb63280a30ea9154e5176321da94ee
ms.contentlocale: de-de
ms.lasthandoff: 11/03/2017

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="b6276-103">MwSt-Berichterstattung für Europa</span><span class="sxs-lookup"><span data-stu-id="b6276-103">VAT reporting for Europe</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b6276-104">Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung  des Mehrwertsteuer-Auszugs für einige europäische Länder.</span><span class="sxs-lookup"><span data-stu-id="b6276-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="b6276-105">Dieses Thema bietet einen allgemeinen Ansatz zum Einrichten und zum Generieren der Mehrwertsteuererklärung.</span><span class="sxs-lookup"><span data-stu-id="b6276-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="b6276-106">Dieser Ansatz ist für Benutzer in juristischen Personen in den folgenden Ländern/Regionen üblich:</span><span class="sxs-lookup"><span data-stu-id="b6276-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="b6276-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="b6276-107">Austria</span></span>
-   <span data-ttu-id="b6276-108">Belgien</span><span class="sxs-lookup"><span data-stu-id="b6276-108">Belgium</span></span>
-   <span data-ttu-id="b6276-109">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="b6276-109">Czech Republic</span></span>
-   <span data-ttu-id="b6276-110">Estland</span><span class="sxs-lookup"><span data-stu-id="b6276-110">Estonia</span></span>
-   <span data-ttu-id="b6276-111">Finnland</span><span class="sxs-lookup"><span data-stu-id="b6276-111">Finland</span></span>
-   <span data-ttu-id="b6276-112">Deutschland</span><span class="sxs-lookup"><span data-stu-id="b6276-112">Germany</span></span>
-   <span data-ttu-id="b6276-113">Lettland</span><span class="sxs-lookup"><span data-stu-id="b6276-113">Latvia</span></span>
-   <span data-ttu-id="b6276-114">Litauen</span><span class="sxs-lookup"><span data-stu-id="b6276-114">Lithuania</span></span>
-   <span data-ttu-id="b6276-115">Niederlande</span><span class="sxs-lookup"><span data-stu-id="b6276-115">Netherlands</span></span>
-   <span data-ttu-id="b6276-116">Schweden</span><span class="sxs-lookup"><span data-stu-id="b6276-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="b6276-117">MwSt.-Auszugs, Überblick</span><span class="sxs-lookup"><span data-stu-id="b6276-117">VAT statement overview</span></span>
<span data-ttu-id="b6276-118">Der MwSt-Auszug basiert auf dem Steuerbuchungsbeträgen.</span><span class="sxs-lookup"><span data-stu-id="b6276-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="b6276-119">Die Generierung eines MwSt. -Auszugs ist Teil des Mehrwertsteuerzahlungsprozesses, der durch die Bank- und Beitragsmehrwertsteuerfunktion implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="b6276-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="b6276-120">Mithilfe dieses Funkltion können Sie die für eine Periode fällige Mehrwertsteuer berechnen.</span><span class="sxs-lookup"><span data-stu-id="b6276-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="b6276-121">Die Ausgleichsberechnung enthält die gebuchte Mehrwertsteuer für den ausgewählten Abrechnungszeitraum für die Steuerbuchungen im Formular .</span><span class="sxs-lookup"><span data-stu-id="b6276-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="b6276-122">Der Prozess zum Berechnen von Daten für einen MwSt.-Auszug basiert auf der Beziehung zwischen  Mehrwertsteuercodes und Mehrwertsteuer-Erklärungscodes, in denen Mehrwertsteuer-Erklärungscodes mit den MwSt.-Auszugsfelder übereinstimmen (oder die Markierungen in XML).</span><span class="sxs-lookup"><span data-stu-id="b6276-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="b6276-123">Für jeden Mehrwertsteuercode sollen Mehrwertsteuer-Erklärungscodes für jede Buchungsart, zum Beispiel steuerpflichtige Verkäufe, steuerpflichtige Einkäufe, steuerpflichtiger Import eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="b6276-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="b6276-124">Hiermit werden Buchungsarten im Feld Mehrwertsteuercodes für Mehrwertsteuer-Berichte im Abschnitt weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="b6276-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="b6276-125">Für jeden Mehrwertsteuer-Erklärungscode soll ein bestimmtes Berichtslayout bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="b6276-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="b6276-126">Gleichzeitig werden Mehrwertsteuercodes auf eine bestimmte Mehrwertsteuerbehörde von Mehrwertsteuer-Ausgleichsperioden verknüpft.</span><span class="sxs-lookup"><span data-stu-id="b6276-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="b6276-127">Für jede Mehrwertsteuer-Behörde sollte ein bestimmtes Berichtslayout bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="b6276-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="b6276-128">Auf diese Weise können nur mit Mehrwertsteuer-Erklärungscodes demselben Berichtslayout, das für die Mehrwertsteuerbehörde in Mehrwertsteuer-Abrechnungszeiträume für den Mehrwertsteuercode errichtet wird, in der Berichtseinstellung des Mehrwertsteuercodes ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="b6276-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="b6276-129">Eine Mehrwertsteuerbuchung, die nach dem Buchen eines Auftrags oder eine Erfassung erstellt wurde, enthält einen Mehrwertsteuercode, eine Mehrwertsteuerquelle, Mehrwertsteuerart und Buchungsbeträge (Steuergrundbetrag und Steuerbetrag in der Buchhaltungswährung, in der Mehrwertsteuerwährung und in der Buchungswährung).</span><span class="sxs-lookup"><span data-stu-id="b6276-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="b6276-130">Durch die Kombination aus Steuerbuchungsattributen, verfassen Buchungsbeträge Gesamtbeträge für die Mehrwertsteuer-Erklärungscodes, die für Mehrwertsteuercodes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b6276-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="b6276-131">Die folgende Abbildung zeigt diese Datenbeziehung.</span><span class="sxs-lookup"><span data-stu-id="b6276-131">The following illustration shows the data relationship.</span></span>

![Diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="b6276-133">MwST-Bericht, Einrichtung</span><span class="sxs-lookup"><span data-stu-id="b6276-133">VAT statement setup</span></span>
<span data-ttu-id="b6276-134">Um einen MwSt-Bericht zu zu Erstellen, müssen Sie Folgendes erstellen:</span><span class="sxs-lookup"><span data-stu-id="b6276-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="b6276-135">MwST-Behörde für MwST-Beichterstattung</span><span class="sxs-lookup"><span data-stu-id="b6276-135">Sales tax authorities for VAT reporting</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](general-ledger/tasks/set-up-sales-tax-authorities). -->
<span data-ttu-id="b6276-136">Bevor Sie Mehrwertsteuer-Erklärungscodes einrichten können, müssen Sie das gewünschte Berichtslayout für die Mehrwertsteuerbehörde auswählen.</span><span class="sxs-lookup"><span data-stu-id="b6276-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="b6276-137">Sie müssen auch das Feld **Berichtslayout** im Bereich **Allgemein** auf der Seite **Mehrwertsteuer-Behörden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="b6276-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="b6276-138">Dieses Layout wird verwendet, wenn Sie Mehrwertsteuer-Erklärungscodes einrichten.</span><span class="sxs-lookup"><span data-stu-id="b6276-138">This layout will be used when you set up sales tax reporting codes.</span></span>

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="b6276-139">Mehrwertsteuer-Erklärungscodes</span><span class="sxs-lookup"><span data-stu-id="b6276-139">Sales tax reporting codes</span></span>

<span data-ttu-id="b6276-140">Mehrwertsteuer-Erklärungscodes werden im Feldcodes MwSt. oder markierter Namen im XML-Format eingegeben.</span><span class="sxs-lookup"><span data-stu-id="b6276-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="b6276-141">Diese Codes werden verwendet, um Beträge für den Bericht zu aggregieren und vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="b6276-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="b6276-142">Wenn Sie das elektronische Berichterstellungsformat des MwSt.-Auszugs konfigurieren, werden die Namen der Ergebnisbeträge verwendet.</span><span class="sxs-lookup"><span data-stu-id="b6276-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="b6276-143">Sie können auf der Seite "Mehrwertsteuer-Erklärungscodes" **Mehrwertsteuer-Erklärungscodes** erstellen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="b6276-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="b6276-144">Sie müssen jedem Code ein Berichtslayout zuweisen.</span><span class="sxs-lookup"><span data-stu-id="b6276-144">You must assign each code a report layout.</span></span> <span data-ttu-id="b6276-145">Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister **Berichtseinstellungen** auf der Seite **Mehrwertsteuercode** auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="b6276-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="b6276-146">Mehrwertsteuercodes für MwSt-Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="b6276-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the **Sales tax codes** page. The following table describes the transaction types in the report setup for sales tax codes. The calculation includes transactions for all types of sources except sales tax.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b6276-147"><strong>Buchungstyp</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-147"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="b6276-148"><strong>Die Buchungsart sowie eine Beschreibung der Buchungsart auf dem Buchungstyp</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-148"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-149"><strong>Steuerpflichtiger Umsatz</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-149"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="b6276-150">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-150">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-151">Das Fälligkeitsdatum für die ausgewählte Periode/</span><span class="sxs-lookup"><span data-stu-id="b6276-151">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="b6276-152">Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>)..</span><span class="sxs-lookup"><span data-stu-id="b6276-152">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="b6276-153">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-153">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-154"><strong>Steuerfreier Verkauf</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-154"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="b6276-155">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-155">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-156">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-156">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-157">Der Verkauf erfolgt im Ausland <strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>)..</span><span class="sxs-lookup"><span data-stu-id="b6276-157">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="b6276-158">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-158">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-159"><strong>Mehrwertsteuer</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-159"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="b6276-160">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-160">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-161">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-161">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-162">Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>)..</span><span class="sxs-lookup"><span data-stu-id="b6276-162">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="b6276-163">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-163">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-164"><strong>Steuerpflichtige Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-164"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="b6276-165">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-165">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-166">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-166">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-167">Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>)..</span><span class="sxs-lookup"><span data-stu-id="b6276-167">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="b6276-168">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-168">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-169"><strong>Steuerbefreite Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-169"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="b6276-170">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-170">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-171">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-171">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-172">Der Verkauf erfolgt im Ausland <strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>)..</span><span class="sxs-lookup"><span data-stu-id="b6276-172">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="b6276-173">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-173">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-174"><strong>Mehrwertsteuer auf Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-174"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="b6276-175">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-175">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-176">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-176">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-177">Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>)..</span><span class="sxs-lookup"><span data-stu-id="b6276-177">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="b6276-178">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-178">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-179"><strong>Steuerpflichtige Einkäufe</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-179"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="b6276-180">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-180">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-181">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-181">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-182">Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="b6276-182">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="b6276-183">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-183">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-184"><strong>Steuerfreier Einkauf</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-184"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="b6276-185">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-185">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-186">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-186">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-187">Der Kauf erfolgt im Ausland <strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>)..</span><span class="sxs-lookup"><span data-stu-id="b6276-187">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="b6276-188">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-188">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-189"><strong>Vorsteuer</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-189"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="b6276-190">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-190">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-191">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-191">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-192">Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="b6276-192">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="b6276-193">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-193">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-194"><strong>Steuerpflichtige Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-194"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="b6276-195">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-195">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-196">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-196">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-197">Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="b6276-197">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="b6276-198">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-198">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-199"><strong>Steuerbefreite Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-199"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="b6276-200">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-200">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-201">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-201">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-202">Der Kauf erfolgt im Ausland <strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>)..</span><span class="sxs-lookup"><span data-stu-id="b6276-202">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="b6276-203">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-203">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-204"><strong>Mehrwertsteuer auf Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-204"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="b6276-205">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-205">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-206">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-206">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-207">Der Verkauf erfolgt inländisch <strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="b6276-207">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="b6276-208">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-208">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-209"><strong>Steuerpflichtiger Import</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-209"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="b6276-210">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-210">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-211">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-211">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-212"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-212"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="b6276-213">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-213">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-214"><strong>Gegenkonto zum steuerpflichtigen Import</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-214"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="b6276-215">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-215">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-216">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-216">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-217"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-217"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="b6276-218">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-218">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-219"><strong>Steuerpflichtige Importgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-219"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="b6276-220">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-220">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-221">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-221">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="b6276-222">e</span><span class="sxs-lookup"><span data-stu-id="b6276-222">e</span></span><li><span data-ttu-id="b6276-223"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-223"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="b6276-224">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-224">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-225"><strong>Gegenkonto zur steuerpflichtigen Import-Gutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-225"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="b6276-226">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-226">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-227">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-227">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-228">Steuerart ist <strong>Steuernutzung</strong>.</span><span class="sxs-lookup"><span data-stu-id="b6276-228">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="b6276-229">d</span><span class="sxs-lookup"><span data-stu-id="b6276-229">d</span></span><li><span data-ttu-id="b6276-230">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-230">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b6276-231"><strong>Verbrauchssteuer</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-231"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="b6276-232">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-232">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-233">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-233">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-234"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-234"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="b6276-235">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-235">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b6276-236"><strong>Gegenkonto Verbrauchssteuer</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-236"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="b6276-237">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="b6276-237">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="b6276-238">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="b6276-238">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="b6276-239"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="b6276-239"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="b6276-240">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="b6276-240">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="b6276-241">Für die Tabelle oben wird angenommen, dass die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="b6276-241">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="b6276-242">Der Steuergrundbetrag ist ein Transaktionsbetrag aus dem Feld **Ursprung in der Buchungswährung**.</span><span class="sxs-lookup"><span data-stu-id="b6276-242">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="b6276-243">Der Steuerbetrag ist ein Transaktionsbetrag aus dem Feld **Aktueller Mehrwertsteuerbetrag in der  Buchungswährung**.</span><span class="sxs-lookup"><span data-stu-id="b6276-243">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="b6276-244">Konfigurieren Sie das ER-Modell und -Format für den Bericht</span><span class="sxs-lookup"><span data-stu-id="b6276-244">Configure the ER model and format for the report</span></span>

<span data-ttu-id="b6276-245">Sie können Elektronische Berichterstattung (ER) verwenden, um Auszüge und Berichte zu konfigurieren und verschiedene elektronische Datenformate zu exportieren, ohne den X++-Code zu ändern.</span><span class="sxs-lookup"><span data-stu-id="b6276-245">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="b6276-246">Zusätzliche Informationen:</span><span class="sxs-lookup"><span data-stu-id="b6276-246">For additional information:</span></span>

-   [<span data-ttu-id="b6276-247">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="b6276-247">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="b6276-248">Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen</span><span class="sxs-lookup"><span data-stu-id="b6276-248">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   <span data-ttu-id="b6276-249">[[Lokalisierungsanforderungen - Erstellen Sie eine GER-Konfiguration](../../dev-itpro/analytics/electronic-reporting-configuration.md)</span><span class="sxs-lookup"><span data-stu-id="b6276-249">[Localization requirements – Create a GER configuration](../../dev-itpro/analytics/electronic-reporting-configuration.md)</span></span>

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="b6276-250">Länderspezifische Ressourcen für Mehrwertsteuer-Auszüge</span><span class="sxs-lookup"><span data-stu-id="b6276-250">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="b6276-251">Der Mehrwertsteuertyp. im für jedes Land muss den Bedingungen der Gesetzgeber des Lands erfüllen.</span><span class="sxs-lookup"><span data-stu-id="b6276-251">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="b6276-252">Es gibt vordefinierten allgemeine Modelle und Formate der MwSt.-Auszügen für die Länder, die in der weiter unten dargestellten Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="b6276-252">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="b6276-253">Land</span><span class="sxs-lookup"><span data-stu-id="b6276-253">Country</span></span>        | <span data-ttu-id="b6276-254">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b6276-254">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="b6276-255">Österreich</span><span class="sxs-lookup"><span data-stu-id="b6276-255">Austria</span></span>        |  [<span data-ttu-id="b6276-256">MwSt-Berichtdetails für Österreich</span><span class="sxs-lookup"><span data-stu-id="b6276-256">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="b6276-257">Belgien</span><span class="sxs-lookup"><span data-stu-id="b6276-257">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="b6276-258">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="b6276-258">Czech Republic</span></span> |  [<span data-ttu-id="b6276-259">MwSt.-Berichtsdetails für die Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="b6276-259">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="b6276-260">Estland</span><span class="sxs-lookup"><span data-stu-id="b6276-260">Estonia</span></span>        |  [<span data-ttu-id="b6276-261">MwSt-Berichtadetails für Estland</span><span class="sxs-lookup"><span data-stu-id="b6276-261">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="b6276-262">Finnland</span><span class="sxs-lookup"><span data-stu-id="b6276-262">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="b6276-263">Deutschland</span><span class="sxs-lookup"><span data-stu-id="b6276-263">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="b6276-264">Italien</span><span class="sxs-lookup"><span data-stu-id="b6276-264">Italy</span></span>          | [<span data-ttu-id="b6276-265">MwSt-Berichtdetail für Italien</span><span class="sxs-lookup"><span data-stu-id="b6276-265">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="b6276-266">Lettland</span><span class="sxs-lookup"><span data-stu-id="b6276-266">Latvia</span></span>         | [<span data-ttu-id="b6276-267">MwSt-Berichtdetail für Lettland</span><span class="sxs-lookup"><span data-stu-id="b6276-267">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="b6276-268">Litauen</span><span class="sxs-lookup"><span data-stu-id="b6276-268">Lithuania</span></span>      | [<span data-ttu-id="b6276-269">MwSt-Berichtdetail für Litauen</span><span class="sxs-lookup"><span data-stu-id="b6276-269">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="b6276-270">Niederlande</span><span class="sxs-lookup"><span data-stu-id="b6276-270">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="b6276-271">Schweden</span><span class="sxs-lookup"><span data-stu-id="b6276-271">Sweden</span></span>         |                                                                                 |






