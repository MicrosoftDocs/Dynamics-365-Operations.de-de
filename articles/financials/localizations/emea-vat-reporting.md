---
title: "MwSt-Berichterstattung für Europa"
description: "Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung des Mehrwertsteuer-Auszugs für einige europäische Länder."
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 5c5cd61c45eb7cbc6f040f054a99d9a54e1ee854
ms.contentlocale: de-de
ms.lasthandoff: 05/08/2018

---

# <a name="vat-reporting-for-europe"></a><span data-ttu-id="54216-103">MwSt-Berichterstattung für Europa</span><span class="sxs-lookup"><span data-stu-id="54216-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="54216-104">Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung des Mehrwertsteuer-Auszugs für einige europäische Länder.</span><span class="sxs-lookup"><span data-stu-id="54216-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="54216-105">Dieses Thema bietet einen allgemeinen Ansatz zum Einrichten und zum Generieren der Mehrwertsteuererklärung.</span><span class="sxs-lookup"><span data-stu-id="54216-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="54216-106">Dieser Ansatz ist für Benutzer in juristischen Personen in den folgenden Ländern/Regionen üblich:</span><span class="sxs-lookup"><span data-stu-id="54216-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="54216-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="54216-107">Austria</span></span>
-   <span data-ttu-id="54216-108">Belgien</span><span class="sxs-lookup"><span data-stu-id="54216-108">Belgium</span></span>
-   <span data-ttu-id="54216-109">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="54216-109">Czech Republic</span></span>
-   <span data-ttu-id="54216-110">Estland</span><span class="sxs-lookup"><span data-stu-id="54216-110">Estonia</span></span>
-   <span data-ttu-id="54216-111">Finnland</span><span class="sxs-lookup"><span data-stu-id="54216-111">Finland</span></span>
-   <span data-ttu-id="54216-112">Deutschland</span><span class="sxs-lookup"><span data-stu-id="54216-112">Germany</span></span>
-   <span data-ttu-id="54216-113">Lettland</span><span class="sxs-lookup"><span data-stu-id="54216-113">Latvia</span></span>
-   <span data-ttu-id="54216-114">Litauen</span><span class="sxs-lookup"><span data-stu-id="54216-114">Lithuania</span></span>
-   <span data-ttu-id="54216-115">Niederlande</span><span class="sxs-lookup"><span data-stu-id="54216-115">Netherlands</span></span>
-   <span data-ttu-id="54216-116">Schweden</span><span class="sxs-lookup"><span data-stu-id="54216-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="54216-117">MwSt.-Auszugs, Überblick</span><span class="sxs-lookup"><span data-stu-id="54216-117">VAT statement overview</span></span>
<span data-ttu-id="54216-118">Der MwSt-Auszug basiert auf dem Steuerbuchungsbeträgen.</span><span class="sxs-lookup"><span data-stu-id="54216-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="54216-119">Die Generierung eines MwSt. -Auszugs ist Teil des Mehrwertsteuerzahlungsprozesses, der durch die Bank- und Beitragsmehrwertsteuerfunktion implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="54216-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="54216-120">Mithilfe dieses Funkltion können Sie die für eine Periode fällige Mehrwertsteuer berechnen.</span><span class="sxs-lookup"><span data-stu-id="54216-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="54216-121">Die Ausgleichsberechnung enthält die gebuchte Mehrwertsteuer für den ausgewählten Abrechnungszeitraum für die Steuerbuchungen im Formular .</span><span class="sxs-lookup"><span data-stu-id="54216-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="54216-122">Der Prozess zum Berechnen von Daten für einen MwSt.-Auszug basiert auf der Beziehung zwischen Mehrwertsteuercodes und Mehrwertsteuer-Erklärungscodes, in denen Mehrwertsteuer-Erklärungscodes mit den MwSt.-Auszugsfelder übereinstimmen (oder die Markierungen in XML).</span><span class="sxs-lookup"><span data-stu-id="54216-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="54216-123">Für jeden Mehrwertsteuercode sollen Mehrwertsteuer-Erklärungscodes für jede Buchungsart, zum Beispiel steuerpflichtige Verkäufe, steuerpflichtige Einkäufe, steuerpflichtiger Import eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="54216-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="54216-124">Hiermit werden Buchungsarten im Feld Mehrwertsteuercodes für Mehrwertsteuer-Berichte im Abschnitt weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="54216-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="54216-125">Für jeden Mehrwertsteuer-Erklärungscode soll ein bestimmtes Berichtslayout bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="54216-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="54216-126">Gleichzeitig werden Mehrwertsteuercodes auf eine bestimmte Mehrwertsteuerbehörde von Mehrwertsteuer-Ausgleichsperioden verknüpft.</span><span class="sxs-lookup"><span data-stu-id="54216-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="54216-127">Für jede Mehrwertsteuer-Behörde sollte ein bestimmtes Berichtslayout bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="54216-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="54216-128">Auf diese Weise können nur mit Mehrwertsteuer-Erklärungscodes demselben Berichtslayout, das für die Mehrwertsteuerbehörde in Mehrwertsteuer-Abrechnungszeiträume für den Mehrwertsteuercode errichtet wird, in der Berichtseinstellung des Mehrwertsteuercodes ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="54216-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="54216-129">Eine Mehrwertsteuerbuchung, die nach dem Buchen eines Auftrags oder eine Erfassung erstellt wurde, enthält einen Mehrwertsteuercode, eine Mehrwertsteuerquelle, Mehrwertsteuerart und Buchungsbeträge (Steuergrundbetrag und Steuerbetrag in der Buchhaltungswährung, in der Mehrwertsteuerwährung und in der Buchungswährung).</span><span class="sxs-lookup"><span data-stu-id="54216-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="54216-130">Durch die Kombination aus Steuerbuchungsattributen, verfassen Buchungsbeträge Gesamtbeträge für die Mehrwertsteuer-Erklärungscodes, die für Mehrwertsteuercodes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="54216-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="54216-131">Die folgende Abbildung zeigt diese Datenbeziehung.</span><span class="sxs-lookup"><span data-stu-id="54216-131">The following illustration shows the data relationship.</span></span>

![Diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="54216-133">MwST-Bericht, Einrichtung</span><span class="sxs-lookup"><span data-stu-id="54216-133">VAT statement setup</span></span>
<span data-ttu-id="54216-134">Um einen MwSt-Bericht zu zu Erstellen, müssen Sie Folgendes erstellen:</span><span class="sxs-lookup"><span data-stu-id="54216-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="54216-135">MwST-Behörde für MwST-Beichterstattung</span><span class="sxs-lookup"><span data-stu-id="54216-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="54216-136">Bevor Sie Mehrwertsteuer-Erklärungscodes einrichten können, müssen Sie das gewünschte Berichtslayout für die Mehrwertsteuerbehörde auswählen.</span><span class="sxs-lookup"><span data-stu-id="54216-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="54216-137">Sie müssen auch das Feld **Berichtslayout** im Bereich **Allgemein** auf der Seite **Mehrwertsteuer-Behörden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="54216-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="54216-138">Dieses Layout wird verwendet, wenn Sie Mehrwertsteuer-Erklärungscodes einrichten.</span><span class="sxs-lookup"><span data-stu-id="54216-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="54216-139">Mehrwertsteuer-Erklärungscodes</span><span class="sxs-lookup"><span data-stu-id="54216-139">Sales tax reporting codes</span></span>

<span data-ttu-id="54216-140">Mehrwertsteuer-Erklärungscodes werden im Feldcodes MwSt. oder markierter Namen im XML-Format eingegeben.</span><span class="sxs-lookup"><span data-stu-id="54216-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="54216-141">Diese Codes werden verwendet, um Beträge für den Bericht zu aggregieren und vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="54216-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="54216-142">Wenn Sie das elektronische Berichterstellungsformat des MwSt.-Auszugs konfigurieren, werden die Namen der Ergebnisbeträge verwendet.</span><span class="sxs-lookup"><span data-stu-id="54216-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="54216-143">Sie können auf der Seite "Mehrwertsteuer-Erklärungscodes" **Mehrwertsteuer-Erklärungscodes** erstellen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="54216-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="54216-144">Sie müssen jedem Code ein Berichtslayout zuweisen.</span><span class="sxs-lookup"><span data-stu-id="54216-144">You must assign each code a report layout.</span></span> <span data-ttu-id="54216-145">Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister **Berichtseinstellungen** auf der Seite **Mehrwertsteuercode** auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="54216-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="54216-146">Mehrwertsteuercodes für MwSt-Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="54216-146">Sales tax codes for VAT reporting</span></span>

<span data-ttu-id="54216-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Mehrwertsteuercodes</strong>-Seite.</span><span class="sxs-lookup"><span data-stu-id="54216-147"><!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes). You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="54216-148">Die folgende Tabelle beschreibt die Buchungsarten im Bericht, der für Mehrwertsteuercodes eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="54216-148">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="54216-149">Die Berechnung umfasst Buchungen für alle Quellenarten außer Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="54216-149">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="54216-150"><strong>Buchungstyp</strong></span><span class="sxs-lookup"><span data-stu-id="54216-150"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="54216-151"><strong>Die Buchungsart sowie eine Beschreibung der Buchungsart auf dem Buchungstyp</strong></span><span class="sxs-lookup"><span data-stu-id="54216-151"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-152"><strong>Steuerpflichtiger Umsatz</strong></span><span class="sxs-lookup"><span data-stu-id="54216-152"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="54216-153">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-153">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-154">Das Fälligkeitsdatum für die ausgewählte Periode/</span><span class="sxs-lookup"><span data-stu-id="54216-154">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="54216-155">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-155">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="54216-156">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-156">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-157"><strong>Steuerfreier Verkauf</strong></span><span class="sxs-lookup"><span data-stu-id="54216-157"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="54216-158">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-158">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-159">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-159">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-160">Der Verkauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-160">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="54216-161">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-161">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-162"><strong>Mehrwertsteuer</strong></span><span class="sxs-lookup"><span data-stu-id="54216-162"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="54216-163">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-163">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-164">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-164">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-165">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-165">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="54216-166">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-166">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-167"><strong>Steuerpflichtige Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="54216-167"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="54216-168">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-168">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-169">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-169">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-170">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-170">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="54216-171">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-171">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-172"><strong>Steuerbefreite Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="54216-172"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="54216-173">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-173">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-174">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-174">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-175">Der Verkauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-175">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="54216-176">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-176">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-177"><strong>Mehrwertsteuer auf Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="54216-177"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="54216-178">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-178">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-179">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-179">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-180">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-180">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="54216-181">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-181">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-182"><strong>Steuerpflichtige Einkäufe</strong></span><span class="sxs-lookup"><span data-stu-id="54216-182"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="54216-183">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-183">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-184">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-184">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-185">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-185">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="54216-186">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-186">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-187"><strong>Steuerfreier Einkauf</strong></span><span class="sxs-lookup"><span data-stu-id="54216-187"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="54216-188">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-188">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-189">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-189">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-190">Der Kauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-190">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="54216-191">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-191">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-192"><strong>Vorsteuer</strong></span><span class="sxs-lookup"><span data-stu-id="54216-192"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="54216-193">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-193">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-194">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-194">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-195">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-195">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="54216-196">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-196">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-197"><strong>Steuerpflichtige Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="54216-197"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="54216-198">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-198">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-199">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-199">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-200">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-200">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="54216-201">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-201">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-202"><strong>Steuerbefreite Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="54216-202"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="54216-203">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-203">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-204">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-204">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-205">Der Kauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-205">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="54216-206">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-206">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-207"><strong>Mehrwertsteuer auf Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="54216-207"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="54216-208">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-208">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-209">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-209">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-210">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="54216-210">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="54216-211">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-211">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-212"><strong>Steuerpflichtiger Import</strong></span><span class="sxs-lookup"><span data-stu-id="54216-212"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="54216-213">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-213">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-214">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-214">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-215"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="54216-215"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="54216-216">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-216">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-217"><strong>Gegenkonto zum steuerpflichtigen Import</strong></span><span class="sxs-lookup"><span data-stu-id="54216-217"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="54216-218">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-218">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-219">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-219">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-220"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="54216-220"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="54216-221">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-221">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-222"><strong>Steuerpflichtige Importgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="54216-222"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="54216-223">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-223">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-224">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-224">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="54216-225">e</span><span class="sxs-lookup"><span data-stu-id="54216-225">e</span></span><li><span data-ttu-id="54216-226"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="54216-226"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="54216-227">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-227">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-228"><strong>Gegenkonto zur steuerpflichtigen Import-Gutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="54216-228"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="54216-229">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-229">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-230">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-230">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-231">Steuerart ist <strong>Steuernutzung</strong>.</span><span class="sxs-lookup"><span data-stu-id="54216-231">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="54216-232">d</span><span class="sxs-lookup"><span data-stu-id="54216-232">d</span></span><li><span data-ttu-id="54216-233">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-233">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="54216-234"><strong>Verbrauchssteuer</strong></span><span class="sxs-lookup"><span data-stu-id="54216-234"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="54216-235">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-235">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-236">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-236">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-237"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="54216-237"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="54216-238">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-238">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="54216-239"><strong>Gegenkonto Verbrauchssteuer</strong></span><span class="sxs-lookup"><span data-stu-id="54216-239"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="54216-240">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="54216-240">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="54216-241">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="54216-241">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="54216-242"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="54216-242"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="54216-243">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="54216-243">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="54216-244">Für die Tabelle oben wird angenommen, dass die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="54216-244">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="54216-245">Der Steuergrundbetrag ist ein Transaktionsbetrag aus dem Feld **Ursprung in der Buchungswährung**.</span><span class="sxs-lookup"><span data-stu-id="54216-245">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="54216-246">Der Steuerbetrag ist ein Transaktionsbetrag aus dem Feld **Aktueller Mehrwertsteuerbetrag in der Buchungswährung**.</span><span class="sxs-lookup"><span data-stu-id="54216-246">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="54216-247">Konfigurieren Sie das ER-Modell und -Format für den Bericht</span><span class="sxs-lookup"><span data-stu-id="54216-247">Configure the ER model and format for the report</span></span>

<span data-ttu-id="54216-248">Sie können Elektronische Berichterstattung (ER) verwenden, um Auszüge und Berichte zu konfigurieren und verschiedene elektronische Datenformate zu exportieren, ohne den X++-Code zu ändern.</span><span class="sxs-lookup"><span data-stu-id="54216-248">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="54216-249">Zusätzliche Informationen:</span><span class="sxs-lookup"><span data-stu-id="54216-249">For additional information:</span></span>

-   [<span data-ttu-id="54216-250">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="54216-250">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="54216-251">Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen</span><span class="sxs-lookup"><span data-stu-id="54216-251">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="54216-252">Lokalisierungsanforderungen - Erstellen Sie eine GER-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="54216-252">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="54216-253">Länderspezifische Ressourcen für Mehrwertsteuer-Auszüge</span><span class="sxs-lookup"><span data-stu-id="54216-253">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="54216-254">Der Mehrwertsteuertyp. im für jedes Land muss den Bedingungen der Gesetzgeber des Lands erfüllen.</span><span class="sxs-lookup"><span data-stu-id="54216-254">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="54216-255">Es gibt vordefinierten allgemeine Modelle und Formate der MwSt.-Auszügen für die Länder, die in der weiter unten dargestellten Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="54216-255">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="54216-256">Land</span><span class="sxs-lookup"><span data-stu-id="54216-256">Country</span></span>        | <span data-ttu-id="54216-257">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="54216-257">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="54216-258">Österreich</span><span class="sxs-lookup"><span data-stu-id="54216-258">Austria</span></span>        |  [<span data-ttu-id="54216-259">MwSt-Berichtdetails für Österreich</span><span class="sxs-lookup"><span data-stu-id="54216-259">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="54216-260">Belgien</span><span class="sxs-lookup"><span data-stu-id="54216-260">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="54216-261">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="54216-261">Czech Republic</span></span> |  [<span data-ttu-id="54216-262">MwSt.-Berichtsdetails für die Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="54216-262">VAT statement details for Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="54216-263">Estland</span><span class="sxs-lookup"><span data-stu-id="54216-263">Estonia</span></span>        |  [<span data-ttu-id="54216-264">MwSt-Berichtadetails für Estland</span><span class="sxs-lookup"><span data-stu-id="54216-264">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="54216-265">Finnland</span><span class="sxs-lookup"><span data-stu-id="54216-265">Finland</span></span>        |                                                                                 |
| <span data-ttu-id="54216-266">Deutschland</span><span class="sxs-lookup"><span data-stu-id="54216-266">Germany</span></span>        |                                                                                 |
| <span data-ttu-id="54216-267">Italien</span><span class="sxs-lookup"><span data-stu-id="54216-267">Italy</span></span>          | [<span data-ttu-id="54216-268">MwSt-Berichtdetail für Italien</span><span class="sxs-lookup"><span data-stu-id="54216-268">VAT statement details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="54216-269">Lettland</span><span class="sxs-lookup"><span data-stu-id="54216-269">Latvia</span></span>         | [<span data-ttu-id="54216-270">MwSt-Berichtdetail für Lettland</span><span class="sxs-lookup"><span data-stu-id="54216-270">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="54216-271">Litauen</span><span class="sxs-lookup"><span data-stu-id="54216-271">Lithuania</span></span>      | [<span data-ttu-id="54216-272">MwSt-Berichtdetail für Litauen</span><span class="sxs-lookup"><span data-stu-id="54216-272">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="54216-273">Niederlande</span><span class="sxs-lookup"><span data-stu-id="54216-273">Netherlands</span></span>    |                                                                                 |
| <span data-ttu-id="54216-274">Schweden</span><span class="sxs-lookup"><span data-stu-id="54216-274">Sweden</span></span>         |                                                                                 |






