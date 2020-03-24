---
title: Erweiterte Filter- und Abfragesyntax
description: In diesem Thema werden die Filter- und Abfrageoptionen beschrieben, die verfügbar sind, wenn Sie das Dialogfeld Erweitertes Filter/Sortierung oder den Übereinstimmungsoperator im Filterbereich oder die Filter in den Spaltenüberschriften des Gitters verwenden.
author: jasongre
manager: AnnBe
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7a525422a091efe8ea88f42e91dc52488430cfe5
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112190"
---
# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="e9fa9-103">Erweiterte Filter- und Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="e9fa9-103">Advanced filtering and query syntax</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e9fa9-104">In diesem Thema werden die Filter- und Abfrageoptionen beschrieben, die verfügbar sind, wenn Sie das Dialogfeld Erweitertes Filter/Sortierung oder den Operator **Übereinstimmungen** im Filterbereich oder den Spaltenüberschriftsfiltern des Gitters verwenden.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-104">This topic describes the filtering and query options that are available when you use the Advanced filter/sort dialog or the **matches** operator in the Filter pane or grid column header filters.</span></span>

## <a name="advanced-query-syntax"></a><span data-ttu-id="e9fa9-105">Erweiterte Suchsyntax</span><span class="sxs-lookup"><span data-stu-id="e9fa9-105">Advanced query syntax</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e9fa9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9fa9-106">Syntax</span></span></th>
<th><span data-ttu-id="e9fa9-107">Zeichenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="e9fa9-107">Character description</span></span></th>
<th><span data-ttu-id="e9fa9-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9fa9-108">Description</span></span></th>
<th><span data-ttu-id="e9fa9-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e9fa9-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e9fa9-110"><em>Wert</em></span><span class="sxs-lookup"><span data-stu-id="e9fa9-110"><em>value</em></span></span></td>
<td><span data-ttu-id="e9fa9-111">Gleich dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-112">Geben Sie den zu suchenden Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="e9fa9-113">Mit der Zeichenfolge <strong>Schnepf</strong> wird der Begriff &quot;Schnepf&quot; gefunden.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-114">!<em>Wert</em> (Ausrufezeichen)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="e9fa9-115">Ungleich dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-116">Geben Sie vor dem auszuschließenden Wert ein Ausrufezeichen ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="e9fa9-117"><strong>!Schnepf</strong> findet alle Werte außer &quot;Schnepf&quot; gefunden.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-118"><em>Von-Wert</em>..<em>Bis-Wert</em> (zwei Punkte)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="e9fa9-119">Zwischen zwei eingegebenen Werten, die von zwei Punkten getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="e9fa9-120">Geben Sie den "Von-Wert", zwei Punkte und dann den "Bis-Wert" ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="e9fa9-121"><strong>1..10</strong> findet alle Werte von 1 bis 10.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="e9fa9-122">In einem Zeichenfolgenfeld findet <strong>A..C</strong> alle Werte, die mit &quot;A&quot; und &quot;B&quot; beginnen, sowie Werte, die genau gleich &quot;C&quot; sind.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="e9fa9-123">Diese Abfrage findet beispielsweise nicht &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="e9fa9-124">Wenn Sie alle Werte von &quot;A<em>&quot; bis &quot;C</em>&quot;, suchen, geben Sie also <strong>A..D</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-124">To find all values from &quot;A<em>&quot; through &quot;C</em>&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-125">..<em>Wert</em> (zwei Punkte)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="e9fa9-126">Kleiner oder gleich dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-127">Geben Sie zwei Punkte und dann den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="e9fa9-128"><strong>..1000</strong> sucht alle Zahlen, die kleiner oder gleich 1000 sind, wie &quot;100&quot;, &quot;999.95&quot;, und &quot;1,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-129"><em>Wert</em>..</span><span class="sxs-lookup"><span data-stu-id="e9fa9-129"><em>value</em>..</span></span> <span data-ttu-id="e9fa9-130">(zwei Punkte)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-130">(double period)</span></span></td>
<td><span data-ttu-id="e9fa9-131">Größer oder gleich dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-132">Geben Sie den Wert und dann zwei Punkte ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="e9fa9-133"><strong>1000</strong></span><span class="sxs-lookup"><span data-stu-id="e9fa9-133"><strong>1000..</strong></span></span> <span data-ttu-id="e9fa9-134">sucht alle Zahlen, die größer oder gleich 1000 sind, z. B. &quot;1,000&quot;, &quot;1,000.01&quot;, und &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-135">&gt;<em>Wert</em> (Zeichen "größer als")</span><span class="sxs-lookup"><span data-stu-id="e9fa9-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="e9fa9-136">Größer als der eingegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-137">Geben Sie das Zeichen "größer als (<strong>&gt;</strong>) und dann den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="e9fa9-138"><strong>&gt;1000</strong> sucht alle Zahlen, die größer als 1000 sind, wie &quot;1000.01&quot;, &quot;20,000&quot;, und &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-139">&lt;<em>Wert</em> (Zeichen "kleiner als")</span><span class="sxs-lookup"><span data-stu-id="e9fa9-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="e9fa9-140">Kleiner als der eingegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-141">Geben Sie das Zeichen "kleiner als (<strong>&lt;</strong>) und dann den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="e9fa9-142"><strong>&lt;1000</strong> sucht alle Zahlen, die kleiner als 1000 sind, wie z. B. &quot;999.99&quot;, &quot;1&quot;, und &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-143"><em>Wert</em>\* (Stern)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-143"><em>value</em>\* (asterisk)</span></span></td>
<td><span data-ttu-id="e9fa9-144">Beginnend ab dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-145">Geben Sie einen Anfangswert und dann einen Stern (<strong>\*</strong>) ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-145">Type the starting value and then an asterisk (<strong>\*</strong>).</span></span></td>
<td><span data-ttu-id="e9fa9-146"><strong>S\*</strong> findet alle Zeichenfolgen, die mit &quot;S&quot; beginnen, wie &quot;Stockholm&quot;, &quot;Sydney&quot;, und &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-146"><strong>S\*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-147">\*<em>Wert</em> (Stern)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-147">\*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="e9fa9-148">Endet mit dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-149">Geben Sie einen Stern und dann den Endwert ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="e9fa9-150"><strong>\*Osten</strong> findet alle Zeichenfolgen, die auf  &quot;Ostent&quot; enden, wie  &quot;Nordosten&quot; und &quot;Südosten&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-150"><strong>\*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-151">*<em>Wert</em>* (Stern)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="e9fa9-152">Enthält den eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="e9fa9-153">Geben Sie einen Stern, den Wert und dann einen weiteren Stern ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="e9fa9-154"><strong>*st*</strong>  findet alle Zeichenfolgen, die &quot;st&quot; enthalten, wie &quot;Nordosten&quot; und &quot;Südosten&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-155">?</span><span class="sxs-lookup"><span data-stu-id="e9fa9-155">?</span></span> <span data-ttu-id="e9fa9-156">(Fragezeichen)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-156">(question mark)</span></span></td>
<td><span data-ttu-id="e9fa9-157">Enthält ein oder mehrere unbekannte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="e9fa9-158">Geben Sie an der Position des unbekannten Zeichens im Wert ein Fragezeichen ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="e9fa9-159"><strong>Sm?th</strong> findet das System &quot;Smith&quot; und &quot;Smyth&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-160"><em>Wert</em>,<em>Wert</em> (Komma)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="e9fa9-161">Vergleicht die Werte, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="e9fa9-162">Geben Sie alle Kriterien durch Kommas getrennt an.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="e9fa9-163"><strong>A, D, F, G</strong> findet genau &quot;A&quot;, &quot;D&quot;, &quot;F&quot; und &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="e9fa9-164"><strong>10, 20, 30, 100</strong> findet genau &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-165">"" (zwei doppelte Anführungszeichen)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-165">"" (two double quotes)</span></span></td>
<td><span data-ttu-id="e9fa9-166">Übereinstimmung mit einem leeren Wert</span><span class="sxs-lookup"><span data-stu-id="e9fa9-166">Matching a blank value</span></span></td>
<td><span data-ttu-id="e9fa9-167">Geben Sie zwei aufeinanderfolgende doppelte Anführungszeichen ein, um in diesem Feld nach leeren Werten zu filtern.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-167">Type two consecutive double quotes to filter for blank values in that field.</span></span></td>
<td><span data-ttu-id="e9fa9-168">Zwei aufeinanderfolgende doppelte Anführungszeichen (<strong>""</strong>) finden Zeilen ohne Wert für die aktuelle Spalte.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-168">Two consecutive double quotes (<strong>""</strong>) finds rows with no value for the current column.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-169">(<span class="code">Finance and Operations-Abfrage</span>) (Finance and Operations-Abfrage zwischen Klammern)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-169">(<span class="code">Finance and Operations query</span>) (Finance and Operations query between parentheses)</span></span></td>
<td><span data-ttu-id="e9fa9-170">Übereinstimmung mit einer definierten Abfrage</span><span class="sxs-lookup"><span data-stu-id="e9fa9-170">Matching a defined query</span></span></td>
<td><span data-ttu-id="e9fa9-171">Geben Sie eine Abfrage als SQL-Anweisung zwischen Klammern in der Abfragesprache Finance and Operations ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-171">Type a query as an SQL statement between parentheses using the Finance and Operations query language.</span></span></td>
  <td><span data-ttu-id="e9fa9-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span><span class="sxs-lookup"><span data-stu-id="e9fa9-172"><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong></span></span><br><br> 
       <span data-ttu-id="e9fa9-173">als Syntaxbeispiel für eine Filterbedingung auf ein Feld aus der Stammdatensammlung sowie ein Feld aus einer anderen Datenquelle (für die Seite Alle Kunden)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-173">as an example of syntax for a filter condition on a field from the root datasource as well as a field from a different datasource (for the All customers page)</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-174">Di</span><span class="sxs-lookup"><span data-stu-id="e9fa9-174">T</span></span></td>
<td><span data-ttu-id="e9fa9-175">Datum von heute</span><span class="sxs-lookup"><span data-stu-id="e9fa9-175">Today's date</span></span></td>
<td><span data-ttu-id="e9fa9-176">Geben Sie <strong>T</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-176">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="e9fa9-177"><strong>T</strong> gleicht heutiges Datum ab.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-177"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-178">(methodName (Parameter)) (<strong>SysQueryRangeUtil</strong>-Methode in Klammern)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-178">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="e9fa9-179">Abgleichen des Werts oder Wertebereichs, der mit den Parametern der <strong>SysQueryRangeUtil</strong>-Methode angegeben wird</span><span class="sxs-lookup"><span data-stu-id="e9fa9-179">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="e9fa9-180">Geben Sie eine <strong>SysQueryRangeUtil</strong>-Methode mit Parametern ein, die den Wert oder Wertebereich angeben.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-180">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td>
<ol>
<li><span data-ttu-id="e9fa9-181">Klicken Sie auf <strong>Debitoren</strong> &gt; <strong>Rechnungen</strong> &gt; <strong>Offene Debitorenrechnungen</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-181">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-182">Drücken Sie STRG+UMSCHALT+F3, um die Seite <strong>Abfrage</strong> zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-182">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="e9fa9-183">Klicken Sie auf der Registerkarte <strong>Bereich</strong> auf <strong>Hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-183">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-184">Wählen Sie im Feld <strong>Tabelle</strong> die Option <strong>Offene Debitorenbuchungen</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-184">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-185">Wählen Sie im Feld <strong>Feld</strong> <strong>Fälligkeitsdatum</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-185">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-186">Geben Sie im Feld <strong>Kriterien</strong> <strong>(yearRange(-2,0))</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-186">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-187">Klicken Sie auf <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-187">Click <strong>OK</strong>.</span></span> <span data-ttu-id="e9fa9-188">Die Listenseite wird aktualisiert und listet die Rechnungen auf, die den Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-188">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="e9fa9-189">Bei diesem speziellen Beispiel werden Rechnungen auf der Listenseite aufgeführt, die in den vorherigen zwei Jahren fällig waren.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-189">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="e9fa9-190">In der Tabelle im nächsten Abschnitt finden Sie zusätzliche Details zu <strong>SysQueryRangeUtil</strong>-Datumsmethoden und einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-190">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="e9fa9-191">Erweiterte Datumsabfragen, die SysQueryRangeUtil-Methoden verwenden</span><span class="sxs-lookup"><span data-stu-id="e9fa9-191">Advanced date queries that use SysQueryRangeUtil methods</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="e9fa9-192">Methode</span><span class="sxs-lookup"><span data-stu-id="e9fa9-192">Method</span></span></th>
<th><span data-ttu-id="e9fa9-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e9fa9-193">Description</span></span></th>
<th><span data-ttu-id="e9fa9-194">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e9fa9-194">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="e9fa9-195">Tag (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-195">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="e9fa9-196">Suchen Sie ein Datum im Verhältnis zum Sitzungsdatum.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-196">Find a date relative to the session date.</span></span> <span data-ttu-id="e9fa9-197">Positive Werte geben zukünftige Daten an und negative Werte geben ältere Datumsangaben an.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-197">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9fa9-198"><strong>Morgen</strong> – Eingabe <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-198"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-199"><strong>Heute</strong> – Eingabe <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-199"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-200"><strong>Gestern</strong> – Eingabe <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-200"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-201">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="e9fa9-202">Suchen Sie einen Datumsbereich im Verhältnis zum Sitzungsdatum.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-202">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="e9fa9-203">Positive Werte geben zukünftige Daten an und negative Werte geben ältere Datumsangaben an.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-203">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9fa9-204"><strong>Letzte 30 Tage</strong> – Eingabe <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-204"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-205"><strong>Vorherige 30 Tage und kommende 30 Tage</strong> – Eingabe <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-205"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-206">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="e9fa9-207">Suchen Sie alle Datumsangaben nach dem angegebenen relativen Datum.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-207">Find all dates after the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9fa9-208"><strong>Mehr als 30 Tage ab jetzt</strong> – Eingabe <strong>(GreaterThanDate (30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-208"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-209">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="e9fa9-209">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="e9fa9-210">Suchen Sie alle Datums-/Uhrzeiteinträge nach der aktuellen Zeit.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-210">Find all date/time entries after the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9fa9-211"><strong>Alle zukünftigen Daten/Uhrzeiten</strong> – Eingabe <strong>(GreaterThanUtcNow ())</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-211"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-212">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="e9fa9-213">Suchen Sie alle Datumsangaben vor dem angegebenen relativen Datum.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-213">Find all dates before the specified relative date.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9fa9-214"><strong>Weniger als sieben Tage ab jetzt</strong> – Eingabe <strong>(LessThanDate (7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-214"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-215">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="e9fa9-215">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="e9fa9-216">Suchen Sie alle Datums-/Uhrzeiteinträge vor der aktuellen Zeit.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-216">Find all date/time entries before the current time.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9fa9-217"><strong>Alle vergangenen Daten/Uhrzeiten</strong> – Eingabe <strong>(LessThanUtcNow ())</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-217"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-218">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="e9fa9-219">Suchen Sie einen Datumsbereich auf Grundlage von Monaten relativ zum aktuellen Monat.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-219">Find a range of dates, based on months relative to the current month.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9fa9-220"><strong>Vorherige zwei Monate</strong> – Eingabe <strong>(MonthRange (- 2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-220"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-221"><strong>Nächste drei Monate</strong> – Eingabe <strong>(MonthRange (0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-221"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="e9fa9-222">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="e9fa9-222">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="e9fa9-223">Suchen Sie einen Datumsbereich auf Grundlage von Jahren relativ zum aktuellen Jahr.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-223">Find a range of dates, based on years relative to the current year.</span></span></td>
<td>
<ul>
<li><span data-ttu-id="e9fa9-224"><strong>Nächstes Jahr</strong> – Eingabe <strong>(YearRange (0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-224"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="e9fa9-225"><strong>Vorheriges Jahr</strong> – Eingabe <strong>(YearRange (-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="e9fa9-225"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>
