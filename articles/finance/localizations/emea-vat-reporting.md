---
title: MwSt-Berichterstattung für Europa
description: Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung des Mehrwertsteuer-Auszugs für einige europäische Länder.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxAuthority, TaxReportCollection, TaxTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 266844
ms.search.region: Austria, Belgium, Czech Republic, Estonia, Finland, Germany, Latvia, Lithuania, Netherlands, Sweden
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 2a9b5bafb70883d9daf35a7d5a9107d7aee23469
ms.sourcegitcommit: 98ef9178b28cd548f08f8c32255636e6e09b25f2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/22/2020
ms.locfileid: "3395985"
---
# <a name="vat-reporting-for-europe"></a><span data-ttu-id="c9811-103">MwSt-Berichterstattung für Europa</span><span class="sxs-lookup"><span data-stu-id="c9811-103">VAT reporting for Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9811-104">Dieses Thema enthält allgemeine Informationen zum Einrichten und Generierung des Mehrwertsteuer-Auszugs für einige europäische Länder.</span><span class="sxs-lookup"><span data-stu-id="c9811-104">This topic provides general information about setting up and generating the value-added tax (VAT) statement for some European countries.</span></span>

<span data-ttu-id="c9811-105">Dieses Thema bietet einen allgemeinen Ansatz zum Einrichten und zum Generieren der Mehrwertsteuererklärung.</span><span class="sxs-lookup"><span data-stu-id="c9811-105">This topic provides a generic approach to setting up and generating the VAT statement.</span></span> <span data-ttu-id="c9811-106">Dieser Ansatz ist für Benutzer in juristischen Personen in den folgenden Ländern/Regionen üblich:</span><span class="sxs-lookup"><span data-stu-id="c9811-106">This approach is common for users in legal entities in the following countries/regions:</span></span>

-   <span data-ttu-id="c9811-107">Österreich</span><span class="sxs-lookup"><span data-stu-id="c9811-107">Austria</span></span>
-   <span data-ttu-id="c9811-108">Belgien</span><span class="sxs-lookup"><span data-stu-id="c9811-108">Belgium</span></span>
-   <span data-ttu-id="c9811-109">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="c9811-109">Czech Republic</span></span>
-   <span data-ttu-id="c9811-110">Estland</span><span class="sxs-lookup"><span data-stu-id="c9811-110">Estonia</span></span>
-   <span data-ttu-id="c9811-111">Finnland</span><span class="sxs-lookup"><span data-stu-id="c9811-111">Finland</span></span>
-   <span data-ttu-id="c9811-112">Deutschland</span><span class="sxs-lookup"><span data-stu-id="c9811-112">Germany</span></span>
-   <span data-ttu-id="c9811-113">Lettland</span><span class="sxs-lookup"><span data-stu-id="c9811-113">Latvia</span></span>
-   <span data-ttu-id="c9811-114">Litauen</span><span class="sxs-lookup"><span data-stu-id="c9811-114">Lithuania</span></span>
-   <span data-ttu-id="c9811-115">Niederlande</span><span class="sxs-lookup"><span data-stu-id="c9811-115">Netherlands</span></span>
-   <span data-ttu-id="c9811-116">Schweden</span><span class="sxs-lookup"><span data-stu-id="c9811-116">Sweden</span></span>

## <a name="vat-statement-overview"></a><span data-ttu-id="c9811-117">MwSt.-Auszugs, Überblick</span><span class="sxs-lookup"><span data-stu-id="c9811-117">VAT statement overview</span></span>
<span data-ttu-id="c9811-118">Der MwSt-Auszug basiert auf dem Steuerbuchungsbeträgen.</span><span class="sxs-lookup"><span data-stu-id="c9811-118">The VAT statement is based on tax transactions’ amounts.</span></span> <span data-ttu-id="c9811-119">Die Generierung eines MwSt. -Auszugs ist Teil des Mehrwertsteuerzahlungsprozesses, der durch die Bank- und Beitragsmehrwertsteuerfunktion implementiert ist.</span><span class="sxs-lookup"><span data-stu-id="c9811-119">The process of generating a VAT statement is part of the Sales tax payment process, which is implemented through the Settle and post sales tax function.</span></span> <span data-ttu-id="c9811-120">Mithilfe dieses Funkltion können Sie die für eine Periode fällige Mehrwertsteuer berechnen.</span><span class="sxs-lookup"><span data-stu-id="c9811-120">This function calculates the sales tax that is due for a given period.</span></span> <span data-ttu-id="c9811-121">Die Ausgleichsberechnung enthält die gebuchte Mehrwertsteuer für den ausgewählten Abrechnungszeitraum für die Steuerbuchungen im Formular .</span><span class="sxs-lookup"><span data-stu-id="c9811-121">The settlement calculation includes the posted sales tax for the selected settlement period for the tax transactions.</span></span> <span data-ttu-id="c9811-122">Der Prozess zum Berechnen von Daten für einen MwSt.-Auszug basiert auf der Beziehung zwischen Mehrwertsteuercodes und Mehrwertsteuer-Erklärungscodes, in denen Mehrwertsteuer-Erklärungscodes mit den MwSt.-Auszugsfelder übereinstimmen (oder die Markierungen in XML).</span><span class="sxs-lookup"><span data-stu-id="c9811-122">The process for calculating data for a VAT statement is based on the relationship between sales tax codes and sales tax reporting codes, where sales tax reporting codes match the VAT statements boxes (or tags in XML).</span></span> <span data-ttu-id="c9811-123">Für jeden Mehrwertsteuercode sollen Mehrwertsteuer-Erklärungscodes für jede Buchungsart, zum Beispiel steuerpflichtige Verkäufe, steuerpflichtige Einkäufe, steuerpflichtiger Import eingerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="c9811-123">For each sales tax code, sales tax reporting codes should be set up for each type of transaction, such as taxable sales, taxable purchases, taxable import.</span></span> <span data-ttu-id="c9811-124">Hiermit werden Buchungsarten im Feld Mehrwertsteuercodes für Mehrwertsteuer-Berichte im Abschnitt weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="c9811-124">These type of transactions are described in the Sales tax codes for VAT reporting section later in this topic.</span></span>

<span data-ttu-id="c9811-125">Für jeden Mehrwertsteuer-Erklärungscode soll ein bestimmtes Berichtslayout bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="c9811-125">For each sales tax reporting code, a specific report layout should be determined.</span></span> <span data-ttu-id="c9811-126">Gleichzeitig werden Mehrwertsteuercodes auf eine bestimmte Mehrwertsteuerbehörde von Mehrwertsteuer-Ausgleichsperioden verknüpft.</span><span class="sxs-lookup"><span data-stu-id="c9811-126">At the same time, sales tax codes are linked to a specific sales tax authority through sales tax settlement periods.</span></span> <span data-ttu-id="c9811-127">Für jede Mehrwertsteuer-Behörde sollte ein bestimmtes Berichtslayout bestimmt werden.</span><span class="sxs-lookup"><span data-stu-id="c9811-127">For every sales tax authority, a report layout should be determined.</span></span> <span data-ttu-id="c9811-128">Auf diese Weise können nur mit Mehrwertsteuer-Erklärungscodes demselben Berichtslayout, das für die Mehrwertsteuerbehörde in Mehrwertsteuer-Abrechnungszeiträume für den Mehrwertsteuercode errichtet wird, in der Berichtseinstellung des Mehrwertsteuercodes ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="c9811-128">Thus, only sales tax reporting codes with the same report layout that is set up for a sales tax authority in sales tax settlement periods for the sales tax code can be selected in the report setup of the sales tax code.</span></span> <span data-ttu-id="c9811-129">Eine Mehrwertsteuerbuchung, die nach dem Buchen eines Auftrags oder eine Erfassung erstellt wurde, enthält einen Mehrwertsteuercode, eine Mehrwertsteuerquelle, Mehrwertsteuerart und Buchungsbeträge (Steuergrundbetrag und Steuerbetrag in der Buchhaltungswährung, in der Mehrwertsteuerwährung und in der Buchungswährung).</span><span class="sxs-lookup"><span data-stu-id="c9811-129">A sales tax transaction generated upon posting an order or a journal, contains a sales tax code, sales tax source, sales tax direction, and transaction amounts (tax base amount and tax amount in accounting currency, sales-tax currency, and transaction currency).</span></span> <span data-ttu-id="c9811-130">Durch die Kombination aus Steuerbuchungsattributen, verfassen Buchungsbeträge Gesamtbeträge für die Mehrwertsteuer-Erklärungscodes, die für Mehrwertsteuercodes angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c9811-130">Based on the combination of tax transaction attributes, transaction amounts compose total amounts for sales tax reporting codes specified for sales tax codes.</span></span> <span data-ttu-id="c9811-131">Die folgende Abbildung zeigt diese Datenbeziehung.</span><span class="sxs-lookup"><span data-stu-id="c9811-131">The following illustration shows the data relationship.</span></span>

![Diagramm](./media/diagram4.jpg)

## <a name="vat-statement-setup"></a><span data-ttu-id="c9811-133">MwST-Bericht, Einrichtung</span><span class="sxs-lookup"><span data-stu-id="c9811-133">VAT statement setup</span></span>
<span data-ttu-id="c9811-134">Um einen MwSt-Bericht zu zu Erstellen, müssen Sie Folgendes erstellen:</span><span class="sxs-lookup"><span data-stu-id="c9811-134">To generate a VAT statement you must set up the following.</span></span>

### <a name="sales-tax-authorities-for-vat-reporting"></a><span data-ttu-id="c9811-135">MwST-Behörde für MwST-Beichterstattung</span><span class="sxs-lookup"><span data-stu-id="c9811-135">Sales tax authorities for VAT reporting</span></span>

<span data-ttu-id="c9811-136">Bevor Sie Mehrwertsteuer-Erklärungscodes einrichten können, müssen Sie das gewünschte Berichtslayout für die Mehrwertsteuerbehörde auswählen.</span><span class="sxs-lookup"><span data-stu-id="c9811-136">Before you can set up sales tax reporting codes, you must select the correct report layout for the sales tax authority.</span></span> <span data-ttu-id="c9811-137">Sie müssen auch das Feld **Berichtslayout** im Bereich **Allgemein** auf der Seite **Mehrwertsteuer-Behörden** auswählen.</span><span class="sxs-lookup"><span data-stu-id="c9811-137">On the **Sales tax authorities** page, in the **General** section, select a **Report layout**.</span></span> <span data-ttu-id="c9811-138">Dieses Layout wird verwendet, wenn Sie Mehrwertsteuer-Erklärungscodes einrichten.</span><span class="sxs-lookup"><span data-stu-id="c9811-138">This layout will be used when you set up sales tax reporting codes.</span></span>

<!---For general information about setting up a sales tax authority, see [Set up sales tax authorities](../general-ledger/tasks/set-up-sales-tax-authorities.md). -->

### <a name="sales-tax-reporting-codes"></a><span data-ttu-id="c9811-139">Mehrwertsteuer-Erklärungscodes</span><span class="sxs-lookup"><span data-stu-id="c9811-139">Sales tax reporting codes</span></span>

<span data-ttu-id="c9811-140">Mehrwertsteuer-Erklärungscodes werden im Feldcodes MwSt. oder markierter Namen im XML-Format eingegeben.</span><span class="sxs-lookup"><span data-stu-id="c9811-140">Sales tax reporting codes are box codes in the VAT statement or tag names in XML format.</span></span> <span data-ttu-id="c9811-141">Diese Codes werden verwendet, um Beträge für den Bericht zu aggregieren und vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="c9811-141">These codes are used to aggregate and prepare amounts for the report.</span></span> <span data-ttu-id="c9811-142">Wenn Sie das elektronische Berichterstellungsformat des MwSt.-Auszugs konfigurieren, werden die Namen der Ergebnisbeträge verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9811-142">When you configure the electronic reporting format of the VAT statement, the names of the result amounts will be used.</span></span> <span data-ttu-id="c9811-143">Sie können auf der Seite "Mehrwertsteuer-Erklärungscodes" **Mehrwertsteuer-Erklärungscodes** erstellen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="c9811-143">You can create and maintain sales tax reporting codes on the **Sales tax reporting codes** page.</span></span> <span data-ttu-id="c9811-144">Sie müssen jedem Code ein Berichtslayout zuweisen.</span><span class="sxs-lookup"><span data-stu-id="c9811-144">You must assign each code a report layout.</span></span> <span data-ttu-id="c9811-145">Nachdem Sie die Mehrwertsteuer-Erklärungscodes erstellt haben, können Sie auf dem Inforegister **Berichtseinstellungen** auf der Seite **Mehrwertsteuercode** auf sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="c9811-145">After you create the sales tax reporting codes, you can choose the codes in the **Report setup** section on the **Sales tax codes** page.</span></span> <!---For more information, see [Set up sales tax reporting codes](../general-ledger/tasks/set-up-sales-tax-reporting-codes.md).-->

### <a name="sales-tax-codes-for-vat-reporting"></a><span data-ttu-id="c9811-146">Mehrwertsteuercodes für MwSt-Berichterstattung</span><span class="sxs-lookup"><span data-stu-id="c9811-146">Sales tax codes for VAT reporting</span></span>

<!---For general information about setting up sales tax codes, see [Set up sales tax codes](../general-ledger/tasks/set-up-sales-tax-codes.md).--> <span data-ttu-id="c9811-147"> Grundbeträge und Steuerbeträge von Mehrwertsteuerbuchungen können auf Erklärungscodes im MwSt.-Bericht (XML-Markierungen oder Meldungsfelder) zusammengefasst werden.</span><span class="sxs-lookup"><span data-stu-id="c9811-147">Base amounts and tax amounts of sales tax transactions can be aggregated on reporting codes in the VAT statement (XML tags or declaration boxes).</span></span> <span data-ttu-id="c9811-148">Sie können dieses einrichten, indem Sie Mehrwertsteuer-Erklärungscodes für verschiedene Buchungsarten für Mehrwertsteuercodes auf der Seite  <strong>Mehrwertsteuercodes</strong> zuordnen.</span><span class="sxs-lookup"><span data-stu-id="c9811-148">You can set this up by associating sales tax reporting codes for different transaction types for sales tax codes on the <strong>Sales tax codes</strong> page.</span></span> <span data-ttu-id="c9811-149">Die folgende Tabelle beschreibt die Buchungsarten im Bericht, der für Mehrwertsteuercodes eingerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="c9811-149">The following table describes the transaction types in the report setup for sales tax codes.</span></span> <span data-ttu-id="c9811-150">Die Berechnung umfasst Buchungen für alle Quellenarten außer Mehrwertsteuer.</span><span class="sxs-lookup"><span data-stu-id="c9811-150">The calculation includes transactions for all types of sources except sales tax.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9811-151"><strong>Buchungstyp</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-151"><strong>Transaction type</strong></span></span></td>
<td><span data-ttu-id="c9811-152"><strong>Die Buchungsart sowie eine Beschreibung der Buchungsart auf dem Buchungstyp</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-152"><strong>Description of transactions and amounts to be counted on the transaction type</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-153"><strong>Steuerpflichtiger Umsatz</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-153"><strong>Taxable Sales</strong></span></span></td>
<td><span data-ttu-id="c9811-154">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-154">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-155">Das Fälligkeitsdatum für die ausgewählte Periode/</span><span class="sxs-lookup"><span data-stu-id="c9811-155">Transaction date is in the selected period/</span></span></li>
<li><span data-ttu-id="c9811-156">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-156">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="c9811-157">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-157">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-158"><strong>Steuerfreier Verkauf</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-158"><strong>Tax-free sales</strong></span></span></td>
<td><span data-ttu-id="c9811-159">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-159">Sum of <strong>Tax base amounts</strong> of tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-160">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-160">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-161">Der Verkauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-161">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="c9811-162">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-162">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-163"><strong>Mehrwertsteuer</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-163"><strong>Sales tax payable</strong></span></span></td>
<td><span data-ttu-id="c9811-164">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-164">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-165">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-165">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-166">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-166">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="c9811-167">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-167">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-168"><strong>Steuerpflichtige Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-168"><strong>Taxable sales credit note</strong></span></span></td>
<td><span data-ttu-id="c9811-169">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-169">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-170">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-170">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-171">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-171">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="c9811-172">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-172">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-173"><strong>Steuerbefreite Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-173"><strong>Fax exempt sales credit note</strong></span></span></td>
<td><span data-ttu-id="c9811-174">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-174">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-175">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-175">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-176">Der Verkauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Umsatz</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-176">The sale is export (<strong>Tax direction</strong> is <strong>Tax-free sale</strong>).</span></span></li>
<li><span data-ttu-id="c9811-177">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-177">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-178"><strong>Mehrwertsteuer auf Verkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-178"><strong>Sales tax on sales credit note</strong></span></span></td>
<td><span data-ttu-id="c9811-179">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-179">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-180">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-180">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-181">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-181">The sale is domestic (<strong>Tax direction</strong> is <strong>Sales tax payable</strong>).</span></span></li>
<li><span data-ttu-id="c9811-182">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-182">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-183"><strong>Steuerpflichtige Einkäufe</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-183"><strong>Taxable purchases</strong></span></span></td>
<td><span data-ttu-id="c9811-184">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-184">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-185">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-185">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-186">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-186">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="c9811-187">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-187">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-188"><strong>Steuerfreier Einkauf</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-188"><strong>Tax-free purchase</strong></span></span></td>
<td><span data-ttu-id="c9811-189">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-189">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-190">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-190">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-191">Der Kauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-191">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="c9811-192">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-192">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-193"><strong>Vorsteuer</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-193"><strong>Sales tax receivable</strong></span></span></td>
<td><span data-ttu-id="c9811-194">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-194">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-195">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-195">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-196">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-196">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="c9811-197">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-197">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-198"><strong>Steuerpflichtige Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-198"><strong>Taxable purchase credit note</strong></span></span></td>
<td><span data-ttu-id="c9811-199">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-199">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-200">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-200">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-201">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-201">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="c9811-202">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-202">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-203"><strong>Steuerbefreite Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-203"><strong>Tax exempt purchase credit note</strong></span></span></td>
<td><span data-ttu-id="c9811-204">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-204">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-205">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-205">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-206">Der Kauf erfolgt im Ausland (<strong>Steuerart</strong> ist <strong>steuerfreier Einkauf</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-206">The purchase is import (<strong>Tax direction</strong> is <strong>Tax-free purchase</strong>).</span></span></li>
<li><span data-ttu-id="c9811-207">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-207">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-208"><strong>Mehrwertsteuer auf Einkaufsgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-208"><strong>Sales tax on purchase credit note</strong></span></span></td>
<td><span data-ttu-id="c9811-209">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-209">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-210">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-210">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-211">Der Verkauf erfolgt inländisch (<strong>Steuerart</strong> ist <strong>zahlbare Umsatzsteuer</strong>).</span><span class="sxs-lookup"><span data-stu-id="c9811-211">The purchase is domestic (<strong>Tax direction</strong> is <strong>Sales tax receivable</strong>).</span></span></li>
<li><span data-ttu-id="c9811-212">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-212">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-213"><strong>Steuerpflichtiger Import</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-213"><strong>Taxable import</strong></span></span></td>
<td><span data-ttu-id="c9811-214">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-214">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-215">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-215">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-216"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-216"><strong>Tax direction</strong> is <strong>Use tax</strong></span></span></li>
<li><span data-ttu-id="c9811-217">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-217">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-218"><strong>Gegenkonto zum steuerpflichtigen Import</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-218"><strong>Offset taxable import</strong></span></span></td>
<td><span data-ttu-id="c9811-219">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-219">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-220">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-220">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-221"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-221"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="c9811-222">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-222">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-223"><strong>Steuerpflichtige Importgutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-223"><strong>Taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="c9811-224">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-224">Sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-225">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-225">Transaction date is in the selected period.</span></span></li>
<span data-ttu-id="c9811-226">e</span><span class="sxs-lookup"><span data-stu-id="c9811-226">e</span></span><li><span data-ttu-id="c9811-227"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-227"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="c9811-228">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-228">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-229"><strong>Gegenkonto zur steuerpflichtigen Import-Gutschrift</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-229"><strong>Offset taxable import credit note</strong></span></span></td>
<td><span data-ttu-id="c9811-230">Summe der <strong>Steuergrundlagebeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-230">Reversed sum of <strong>Tax base amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-231">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-231">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-232">Steuerart ist <strong>Steuernutzung</strong>.</span><span class="sxs-lookup"><span data-stu-id="c9811-232">Tax direction is <strong>Use tax</strong>.</span></span></li>
<span data-ttu-id="c9811-233">d</span><span class="sxs-lookup"><span data-stu-id="c9811-233">d</span></span><li><span data-ttu-id="c9811-234">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &lt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-234">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &lt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9811-235"><strong>Verbrauchssteuer</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-235"><strong>Use tax</strong></span></span></td>
<td><span data-ttu-id="c9811-236">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-236">Sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-237">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-237">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-238"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-238"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="c9811-239">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-239">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9811-240"><strong>Gegenkonto Verbrauchssteuer</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-240"><strong>Offset use tax</strong></span></span></td>
<td><span data-ttu-id="c9811-241">Summe der <strong>Steuerbeträge</strong> der Steuerbuchungen, die die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="c9811-241">Reversed sum of <strong>Tax amounts</strong> of the tax transactions which satisfy the following conditions:</span></span>
<ul>
<li><span data-ttu-id="c9811-242">Das Fälligkeitsdatum für die ausgewählte Periode.</span><span class="sxs-lookup"><span data-stu-id="c9811-242">Transaction date is in the selected period.</span></span></li>
<li><span data-ttu-id="c9811-243"><strong>Steuerart</strong> ist <strong>Steuernutzung</strong></span><span class="sxs-lookup"><span data-stu-id="c9811-243"><strong>Tax direction</strong> is <strong>Use tax</strong>.</span></span></li>
<li><span data-ttu-id="c9811-244">Die Buchung <strong>Steuergrundbetrag</strong> oder <strong>Steuerbetrag</strong> &gt; 0.</span><span class="sxs-lookup"><span data-stu-id="c9811-244">The transaction <strong>Tax base amount</strong> or <strong>Tax amount</strong> &gt; 0.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

> [!NOTE]
> <span data-ttu-id="c9811-245">Für die Tabelle oben wird angenommen, dass die folgenden Kriterien erfüllt sein:</span><span class="sxs-lookup"><span data-stu-id="c9811-245">For the table above, it is assumed that the following criteria are met:</span></span> 
> -   <span data-ttu-id="c9811-246">Der Steuergrundbetrag ist ein Transaktionsbetrag aus dem Feld **Ursprung in der Buchungswährung**.</span><span class="sxs-lookup"><span data-stu-id="c9811-246">The tax base amount is a transaction amount from the **Origin in Accounting currency** field.</span></span>
> -   <span data-ttu-id="c9811-247">Der Steuerbetrag ist ein Transaktionsbetrag aus dem Feld **Aktueller Mehrwertsteuerbetrag in der Buchungswährung**.</span><span class="sxs-lookup"><span data-stu-id="c9811-247">The tax amount is a transition amount from the **Actual sales tax amount in Accounting currency** field.</span></span>

### <a name="configure-the-er-model-and-format-for-the-report"></a><span data-ttu-id="c9811-248">Konfigurieren Sie das ER-Modell und -Format für den Bericht</span><span class="sxs-lookup"><span data-stu-id="c9811-248">Configure the ER model and format for the report</span></span>

<span data-ttu-id="c9811-249">Sie können Elektronische Berichterstattung (ER) verwenden, um Auszüge und Berichte zu konfigurieren und verschiedene elektronische Datenformate zu exportieren, ohne den X++-Code zu ändern.</span><span class="sxs-lookup"><span data-stu-id="c9811-249">You can use Electronic Reporting (ER) to configure statements and report, and to export data different electronic formats without changing X++ code.</span></span> <span data-ttu-id="c9811-250">Zusätzliche Informationen:</span><span class="sxs-lookup"><span data-stu-id="c9811-250">For additional information:</span></span>

-   [<span data-ttu-id="c9811-251">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="c9811-251">Electronic reporting overview</span></span>](../../dev-itpro/analytics/general-electronic-reporting.md)
-   [<span data-ttu-id="c9811-252">Elektronische Berichterstellungskonfigurationen von Lifecycle Services herunterladen</span><span class="sxs-lookup"><span data-stu-id="c9811-252">Download Electronic reporting configurations from Lifecycle Services</span></span>](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md)
-   [<span data-ttu-id="c9811-253">Lokalisierungsanforderungen - Erstellen Sie eine GER-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="c9811-253">Localization requirements – Create a GER configuration</span></span>](../../dev-itpro/analytics/electronic-reporting-configuration.md)

## <a name="countryspecific-resources-for-vat-statements"></a><span data-ttu-id="c9811-254">Länderspezifische Ressourcen für Mehrwertsteuer-Auszüge</span><span class="sxs-lookup"><span data-stu-id="c9811-254">Countryspecific resources for VAT statements</span></span>
<span data-ttu-id="c9811-255">Der Mehrwertsteuertyp. im für jedes Land muss den Bedingungen der Gesetzgeber des Lands erfüllen.</span><span class="sxs-lookup"><span data-stu-id="c9811-255">The VAT statement for each country must meet the requirements of the country’s legislation.</span></span> <span data-ttu-id="c9811-256">Es gibt vordefinierten allgemeine Modelle und Formate der MwSt.-Auszügen für die Länder, die in der weiter unten dargestellten Tabelle aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="c9811-256">There are predefined general models and formats of VAT statements for the countries listed in the following table.</span></span>


| <span data-ttu-id="c9811-257">Land</span><span class="sxs-lookup"><span data-stu-id="c9811-257">Country</span></span>        | <span data-ttu-id="c9811-258">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c9811-258">Additional information</span></span>                                                          |
|----------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="c9811-259">Österreich</span><span class="sxs-lookup"><span data-stu-id="c9811-259">Austria</span></span>        |  [<span data-ttu-id="c9811-260">MwSt-Berichtdetails für Österreich</span><span class="sxs-lookup"><span data-stu-id="c9811-260">VAT statement details for Austria</span></span>](emea-aut-vat-statement-details.md)         |
| <span data-ttu-id="c9811-261">Belgien</span><span class="sxs-lookup"><span data-stu-id="c9811-261">Belgium</span></span>        |                                                                                 |
| <span data-ttu-id="c9811-262">Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="c9811-262">Czech Republic</span></span> |  [<span data-ttu-id="c9811-263">MwSt.-Abrechnung für die Tschechische Republik</span><span class="sxs-lookup"><span data-stu-id="c9811-263">VAT statement for the Czech Republic</span></span>](emea-cze-vat-statement-details.md)   |
| <span data-ttu-id="c9811-264">Estland</span><span class="sxs-lookup"><span data-stu-id="c9811-264">Estonia</span></span>        |  [<span data-ttu-id="c9811-265">MwSt-Berichtadetails für Estland</span><span class="sxs-lookup"><span data-stu-id="c9811-265">VAT statement details for Estonia</span></span>](emea-est-vat-statement-details.md) |
| <span data-ttu-id="c9811-266">Finnland</span><span class="sxs-lookup"><span data-stu-id="c9811-266">Finland</span></span>        | [<span data-ttu-id="c9811-267">Mehrwertsteuererklärung für Finnland</span><span class="sxs-lookup"><span data-stu-id="c9811-267">Sales tax report for Finland</span></span>](emea-fin-sales-tax-payment-report-finland.md)          |
| <span data-ttu-id="c9811-268">Deutschland</span><span class="sxs-lookup"><span data-stu-id="c9811-268">Germany</span></span>        | [<span data-ttu-id="c9811-269">Umsatzsteuererklärung für Deutschland</span><span class="sxs-lookup"><span data-stu-id="c9811-269">VAT declaration for Germany</span></span>](emea-de-vat-declaration.md)                       |
| <span data-ttu-id="c9811-270">Italien</span><span class="sxs-lookup"><span data-stu-id="c9811-270">Italy</span></span>          | [<span data-ttu-id="c9811-271">MwSt-Abrechnungsdetails für Italien</span><span class="sxs-lookup"><span data-stu-id="c9811-271">VAT statements details for Italy</span></span>](emea-ita-vat-statements-details.md)            |
| <span data-ttu-id="c9811-272">Lettland</span><span class="sxs-lookup"><span data-stu-id="c9811-272">Latvia</span></span>         | [<span data-ttu-id="c9811-273">MwSt-Berichtdetail für Lettland</span><span class="sxs-lookup"><span data-stu-id="c9811-273">VAT statement details for Latvia</span></span>](emea-lva-vat-statement-details.md)           |
| <span data-ttu-id="c9811-274">Litauen</span><span class="sxs-lookup"><span data-stu-id="c9811-274">Lithuania</span></span>      | [<span data-ttu-id="c9811-275">MwSt-Berichtdetail für Litauen</span><span class="sxs-lookup"><span data-stu-id="c9811-275">VAT statement details for Lithuania</span></span>](emea-ltu-vat-statement-details.md)         |
| <span data-ttu-id="c9811-276">Niederlande</span><span class="sxs-lookup"><span data-stu-id="c9811-276">Netherlands</span></span>    | [<span data-ttu-id="c9811-277">Mehrwertsteuererklärung für die Niederlande</span><span class="sxs-lookup"><span data-stu-id="c9811-277">VAT declaration for the Netherlands</span></span>](emea-nl-vat-declaration.md)           |
| <span data-ttu-id="c9811-278">Schweden</span><span class="sxs-lookup"><span data-stu-id="c9811-278">Sweden</span></span>         | [<span data-ttu-id="c9811-279">Mehrwertsteuererklärung für Schweden</span><span class="sxs-lookup"><span data-stu-id="c9811-279">Sales tax report for Sweden</span></span>](emea-swe-sales-tax-payment-report-sweden.md)          |





