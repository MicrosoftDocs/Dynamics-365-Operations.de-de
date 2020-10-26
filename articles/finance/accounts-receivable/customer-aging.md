---
title: Debitorenfälligkeitsbericht
description: Im Debitorenfälligkeitsbericht werden die von Debitoren fälligen Salden sortiert nach Datumsintervall oder Zahlungsfrist angezeigt.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 062e8972c879d770cc4106c2811cd4c16fff0446
ms.sourcegitcommit: 25909c6ad3616e4f75a2fe006057dda18d7cc856
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/09/2020
ms.locfileid: "3974860"
---
# <a name="customer-aging-report"></a><span data-ttu-id="ae324-103">Debitorenfälligkeitsbericht</span><span class="sxs-lookup"><span data-stu-id="ae324-103">Customer aging report</span></span> 

<span data-ttu-id="ae324-104">Im **Debitorenfälligkeitsbericht** werden die von Debitoren fälligen Salden sortiert nach Datumsintervall oder Zahlungsfrist angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae324-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="ae324-105">Wenn dieser Bericht generiert wird, werden die folgenden Standardparameter angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae324-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="ae324-106">Sie können mithilfe der Parameter die Daten filtern, die im Bericht angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ae324-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="ae324-107">Weitere Informationen finden Sie unter [Einrichten von Auflistungen](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="ae324-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="ae324-108">Feld</span><span class="sxs-lookup"><span data-stu-id="ae324-108">Field</span></span></p></th>
<th><p><span data-ttu-id="ae324-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae324-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae324-110"><strong>Abrechnungsklassifizierung</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-111">Wählen Sie die in den Bericht einzuschließenden Abrechnungsklassifizierungen aus.</span><span class="sxs-lookup"><span data-stu-id="ae324-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="ae324-112">**Hinweis:** Dieses Steuerelement ist nur verfügbar, wenn der Konfigurationsschlüssel <STRONG>Öffentlicher Sektor</STRONG> ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="ae324-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae324-113"><strong>Transaktionen ohne Abrechnungsklassifizierung einbeziehen</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-114">Wenn dieses Kontrollkästchen aktiviert ist, werden alle Buchungen ohne zugewiesene Abrechnungsklassifizierungen im Bericht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae324-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="ae324-115">**Hinweis:** Dieses Steuerelement ist nur verfügbar, wenn der Konfigurationsschlüssel <STRONG>Öffentlicher Sektor</STRONG> ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="ae324-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae324-116"><strong>Fälligkeit per</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-117">Geben Sie das Datum ein, das für den aktuellen Fälligkeitsbereich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ae324-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae324-118"><strong>Saldo per</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-119">Geben Sie das Datum ein, für das die Debitorensalden angezeigt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ae324-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="ae324-120">Dies wird auch als Abschnittsdatum für Buchungen bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="ae324-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae324-121"><strong>Startdatum</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-122">Geben Sie ein Datum ein, das im ersten Periodenintervall oder in der Zahlungsfrist liegt und in den Bericht einbezogen werden soll.</span><span class="sxs-lookup"><span data-stu-id="ae324-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae324-123"><strong>Kriterien</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-124">Wählen Sie den Datumstyp aus, auf dem der Bericht basieren soll.</span><span class="sxs-lookup"><span data-stu-id="ae324-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="ae324-125"><strong>Buchungsdatum</strong> – Das Buchungsdatum der ausgewählten Buchungen.</span><span class="sxs-lookup"><span data-stu-id="ae324-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="ae324-126">Dies kann z. B. ein Rechnungsdatum sein, das die Grundlage für die Berechnung des Fälligkeitsdatums ist.</span><span class="sxs-lookup"><span data-stu-id="ae324-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="ae324-127"><strong>Fälligkeitsdatum</strong> – Das Fälligkeitsdatum der Buchungen, basierend auf den Zahlungsbedingungen.</span><span class="sxs-lookup"><span data-stu-id="ae324-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="ae324-128"><strong>Dokumentdatum</strong> – Ein benutzerdefiniertes Dokumentdatum, das die Grundlage für die Berechnung des Fälligkeitsdatums bildet.</span><span class="sxs-lookup"><span data-stu-id="ae324-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae324-129"><strong>Zahlungsfristdefinition</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-130">Wählen Sie eine Zahlungsfristdefinition aus.</span><span class="sxs-lookup"><span data-stu-id="ae324-130">Select an aging period definition.</span></span> <span data-ttu-id="ae324-131">Das Feld <strong>Intervall</strong> wird bei Auswahl einer Zahlungsfristdefinition nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="ae324-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="ae324-132">Zahlungsfristdefinitionen mit mehr als sechs Zahlungsfristen können im gedruckten Bericht nicht verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ae324-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="ae324-133">**Hinweis:** Sie können Zahlungsfristen auf der Seite <STRONG>Zahlungsfristdefinitionen</STRONG> einrichten.</span><span class="sxs-lookup"><span data-stu-id="ae324-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae324-134"><strong>Beschreibung der Zahlungsfrist drucken</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-135">Wählen Sie <strong>Ja</strong> aus, um Zahlungsfristbeschreibungen im Bericht am Anfang jeder Zahlungsfristspalte einzuschließen.</span><span class="sxs-lookup"><span data-stu-id="ae324-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="ae324-136">Wählen Sie <strong>Nein</strong> aus, um den Bericht ohne Spaltenüberschriften zu drucken.</span><span class="sxs-lookup"><span data-stu-id="ae324-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae324-137"><strong>Intervall</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-138">Definieren Sie die zu verwendende Periode durch Eingeben der Anzahl der Tages- oder Monatseinheiten in jeder Periode.</span><span class="sxs-lookup"><span data-stu-id="ae324-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="ae324-139">Wenn beispielsweise Zahlungsfristinformationen nach Woche angezeigt werden sollen, geben Sie in dieses Feld den Wert 7 ein, und wählen Sie im Feld <strong>Tag/Monat</strong> den Eintrag <strong>Tag</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="ae324-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="ae324-140">**Hinweis:** Die in diesem Feld eingegebenen Informationen werden nur verwendet, falls keine Zahlungsfristdefinition ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="ae324-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="ae324-141">Andernfalls wird die Druckrichtung in der Zahlungsfristdefinition definiert.</span><span class="sxs-lookup"><span data-stu-id="ae324-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae324-142"><strong>Tag/Monat</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-143">Wählen Sie die Einheit aus (entweder <strong>Tag</strong> oder <strong>Monat</strong>), mit der die Periode im Feld <strong>Intervall</strong> definiert wird.</span><span class="sxs-lookup"><span data-stu-id="ae324-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae324-144"><strong>Druckrichtung</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-145">Wählen Sie aus, ob die Berechnung der Salden und das Drucken des Fälligkeitsberichts für vergangene oder zukünftige Perioden erfolgen soll.</span><span class="sxs-lookup"><span data-stu-id="ae324-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="ae324-146">Die Datumsangaben werden relativ zum im Feld <strong>Saldo per</strong> ausgewählten Datum ausgewertet.</span><span class="sxs-lookup"><span data-stu-id="ae324-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="ae324-147">Wählen Sie <strong>Rückwärts</strong> aus, um Informationen zu vergangenen Perioden anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ae324-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="ae324-148">Wählen Sie <strong>Vorwärts</strong> aus, um Informationen zu zukünftigen Perioden anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ae324-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>

<span data-ttu-id="ae324-149">**Hinweis:** Die in diesem Feld eingegebenen Informationen werden nur verwendet, falls keine Zahlungsfristdefinition ausgewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="ae324-149">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae324-150"><strong>Detaildaten</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-151">Aktivieren Sie dieses Kontrollkästchen, um die Buchungen aufzulisten, die in den im Bericht angezeigten Salden enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ae324-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae324-152"><strong>Beträge in Buchungswährung einbeziehen</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-153">Aktivieren Sie dieses Kontrollkästchen, um zusätzlich zu Beträgen in der Buchhaltungswährung Beträge in der Buchungswährung einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="ae324-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="ae324-154">Wenn dieses Kontrollkästchen nicht aktiviert ist, werden die Beträge im Bericht nur in der Buchhaltungswährung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae324-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae324-155"><strong>Negativer Saldo</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-156">Aktivieren Sie dieses Kontrollkästchen, um Debitorenkonten mit negativen Salden einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="ae324-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae324-157"><strong>Konten mit Nullsaldo ausschließen</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-158">Aktivieren Sie dieses Kontrollkästchen, um Debitorenkonten mit Nullsaldo auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="ae324-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae324-159"><strong>Zahlungspositionierung</strong></span><span class="sxs-lookup"><span data-stu-id="ae324-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="ae324-160">Aktivieren Sie dieses Kontrollkästchen, um nicht ausgeglichene Zahlungen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ae324-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="ae324-161">Diese werden in der ersten Spalte des Berichts angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae324-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

