---
title: Erweiterte Filter- und Abfragesyntax
description: "In diesem Artikel werden die Filter- und Abfrageoptionen beschrieben, die verfügbar sind, wenn Sie den \"entspricht\"-Operator im Dialogfeld \"Erweitertes Filtern/Sortieren\" verwenden."
author: jasongre
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 20d28e22e4e89d0d864a0cbeaadeb568e73e223e
ms.openlocfilehash: 616366009ce7bf7135704e980becc331617cf5af
ms.contentlocale: de-de
ms.lasthandoff: 07/27/2017

---

# <a name="advanced-filtering-and-query-syntax"></a><span data-ttu-id="11bca-103">Erweiterte Filter- und Abfragesyntax</span><span class="sxs-lookup"><span data-stu-id="11bca-103">Advanced filtering and query syntax</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="11bca-104">In diesem Artikel werden die Filter- und Abfrageoptionen beschrieben, die verfügbar sind, wenn Sie den "entspricht"-Operator im Dialogfeld "Erweitertes Filtern/Sortieren" verwenden.</span><span class="sxs-lookup"><span data-stu-id="11bca-104">This article describes the filtering and query options that are available when you use the "matches" operator in the Advanced filter/sort dialog.</span></span>

<a name="advanced-query-syntax"></a><span data-ttu-id="11bca-105">Erweiterte Suchsyntax</span><span class="sxs-lookup"><span data-stu-id="11bca-105">Advanced query syntax</span></span>
---------------------

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11bca-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="11bca-106">Syntax</span></span></th>
<th><span data-ttu-id="11bca-107">Zeichenbeschreibung</span><span class="sxs-lookup"><span data-stu-id="11bca-107">Character description</span></span></th>
<th><span data-ttu-id="11bca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11bca-108">Description</span></span></th>
<th><span data-ttu-id="11bca-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="11bca-109">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11bca-110"><em>Wert</em></span><span class="sxs-lookup"><span data-stu-id="11bca-110"><em>value</em></span></span></td>
<td><span data-ttu-id="11bca-111">Gleich dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-111">Equal to the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-112">Geben Sie den zu suchenden Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-112">Type the value to find.</span></span></td>
<td><span data-ttu-id="11bca-113">Mit der Zeichenfolge <strong>Schnepf </strong>wird der Begriff &quot;Schnepf&quot; gefunden.</span><span class="sxs-lookup"><span data-stu-id="11bca-113"><strong>Smith</strong> finds &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-114">!<em>Wert</em> (Ausrufezeichen)</span><span class="sxs-lookup"><span data-stu-id="11bca-114">!<em>value</em> (exclamation point)</span></span></td>
<td><span data-ttu-id="11bca-115">Ungleich dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-115">Not equal to the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-116">Geben Sie vor dem auszuschließenden Wert ein Ausrufezeichen ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-116">Type an exclamation point and then the value to exclude.</span></span></td>
<td><span data-ttu-id="11bca-117"><strong>!Schnepf</strong> findet alle Werte außer &quot;Schnepf&quot; gefunden.</span><span class="sxs-lookup"><span data-stu-id="11bca-117"><strong>!Smith</strong> finds all values except &quot;Smith&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-118"><em>Von-Wert</em>..<em>Bis-Wert</em> (zwei Punkte)</span><span class="sxs-lookup"><span data-stu-id="11bca-118"><em>from-value</em>..<em>to-value</em> (double period)</span></span></td>
<td><span data-ttu-id="11bca-119">Zwischen zwei eingegebenen Werten, die von zwei Punkten getrennt werden.</span><span class="sxs-lookup"><span data-stu-id="11bca-119">Between the two values that are separated by double periods</span></span></td>
<td><span data-ttu-id="11bca-120">Geben Sie den "Von-Wert", zwei Punkte und dann den "Bis-Wert" ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-120">Type the from-value, then two periods, and then the to-value.</span></span></td>
<td><span data-ttu-id="11bca-121"><strong>1..10</strong> findet alle Werte von 1 bis 10.</span><span class="sxs-lookup"><span data-stu-id="11bca-121"><strong>1..10</strong> finds all values from 1 through 10.</span></span> <span data-ttu-id="11bca-122">In einem Zeichenfolgenfeld findet <strong>A..C</strong> alle Werte, die mit &quot;A&quot; und &quot;B&quot; beginnen, sowie Werte, die genau gleich &quot;C&quot; sind.</span><span class="sxs-lookup"><span data-stu-id="11bca-122">However, in a string field, <strong>A..C</strong> finds all values that start with &quot;A&quot; and &quot;B&quot;, and values that are exactly equal to &quot;C&quot;.</span></span> <span data-ttu-id="11bca-123">Diese Abfrage findet beispielsweise nicht &quot;Ca&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-123">For example, this query won't find &quot;Ca&quot;.</span></span> <span data-ttu-id="11bca-124">Wenn Sie alle Werte von &quot;A*&quot; bis &quot;C*&quot;, suchen, geben Sie also <strong>A..D</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-124">To find all values from &quot;A*&quot; through &quot;C*&quot;, type <strong>A..D</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-125">..<em>Wert</em> (zwei Punkte)</span><span class="sxs-lookup"><span data-stu-id="11bca-125">..<em>value</em> (double period)</span></span></td>
<td><span data-ttu-id="11bca-126">Kleiner oder gleich dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-126">Less than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-127">Geben Sie zwei Punkte und dann den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-127">Type two periods and then the value.</span></span></td>
<td><span data-ttu-id="11bca-128"><strong>..1000</strong> sucht alle Zahlen, die kleiner oder gleich 1000 sind, wie &quot;100&quot;, &quot;999.95&quot;, und &quot;1,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-128"><strong>..1000</strong> finds any number that is less than or equal to 1000, such as &quot;100&quot;, &quot;999.95&quot;, and &quot;1,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-129"><em>Wert</em>..</span><span class="sxs-lookup"><span data-stu-id="11bca-129"><em>value</em>..</span></span> <span data-ttu-id="11bca-130">(zwei Punkte)</span><span class="sxs-lookup"><span data-stu-id="11bca-130">(double period)</span></span></td>
<td><span data-ttu-id="11bca-131">Größer oder gleich dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-131">Greater than or equal to the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-132">Geben Sie den Wert und dann zwei Punkte ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-132">Type the value and then two periods.</span></span></td>
<td><span data-ttu-id="11bca-133"><strong>1000</strong></span><span class="sxs-lookup"><span data-stu-id="11bca-133"><strong>1000..</strong></span></span> <span data-ttu-id="11bca-134">sucht alle Zahlen, die größer oder gleich 1000 sind, z. B. &quot;1,000&quot;, &quot;1,000.01&quot;, und &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-134">finds any number that is greater than or equal to 1000, such as &quot;1,000&quot;, &quot;1,000.01&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-135">&gt;<em>Wert</em> ((Zeichen "größer als")</span><span class="sxs-lookup"><span data-stu-id="11bca-135">&gt;<em>value</em> (greater than sign)</span></span></td>
<td><span data-ttu-id="11bca-136">Größer als der eingegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-136">Greater than the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-137">Geben Sie das Zeichen "größer als (<strong>&gt;</strong>)  und dann den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-137">Type a greater than sign (<strong>&gt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="11bca-138"><strong>&gt;1000</strong>sucht alle Zahlen, die größer als 1000 sind, wie &quot;1000.01&quot;, &quot;20,000&quot;, und &quot;1,000,000&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-138"><strong>&gt;1000</strong> finds any number that is greater than 1000, such as &quot;1000.01&quot;, &quot;20,000&quot;, and &quot;1,000,000&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-139">&lt;<em>Wert</em>  (Zeichen "kleiner als")</span><span class="sxs-lookup"><span data-stu-id="11bca-139">&lt;<em>value</em> (less than sign)</span></span></td>
<td><span data-ttu-id="11bca-140">Kleiner als der eingegebene Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-140">Less than the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-141">Geben Sie das Zeichen "kleiner als (<strong>&lt;</strong>) und dann den Wert ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-141">Type a less than sign (<strong>&lt;</strong>) and then the value.</span></span></td>
<td><span data-ttu-id="11bca-142"><strong>&lt;1000</strong> sucht alle Zahlen, die kleiner als 1000 sind, wie z&quot;999.99&quot;, &quot;1&quot;, und &quot;-200&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-142"><strong>&lt;1000</strong> finds any number that is less than 1000, such as &quot;999.99&quot;, &quot;1&quot;, and &quot;-200&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-143"><em>Wert</em>* (Stern)</span><span class="sxs-lookup"><span data-stu-id="11bca-143"><em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="11bca-144">Beginnend ab dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-144">Starting from the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-145">Geben Sie einen Anfangswert und dann einen Stern (<strong>*</strong>) ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-145">Type the starting value and then an asterisk (<strong>*</strong>).</span></span></td>
<td><span data-ttu-id="11bca-146"><strong>S*</strong> findet alle Zeichenfolgen, die mit &quot;S&quot; beginnen, wie &quot;Stockholm&quot;, &quot;Sydney&quot;, und &quot;San Francisco&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-146"><strong>S*</strong> finds any string that starts with &quot;S&quot;, such as &quot;Stockholm&quot;, &quot;Sydney&quot;, and &quot;San Francisco&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-147">*<em>Wert</em>* (Stern)</span><span class="sxs-lookup"><span data-stu-id="11bca-147">*<em>value</em> (asterisk)</span></span></td>
<td><span data-ttu-id="11bca-148">Endet mit dem eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-148">Ending with the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-149">Geben Sie einen Stern und dann den Endwert ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-149">Type an asterisk and then the ending value.</span></span></td>
<td><span data-ttu-id="11bca-150"><strong>*Osten</strong> findet alle Zeichenfolgen, die auf  &quot;Ostent&quot; enden, wie  &quot;Nordosten&quot; und &quot;Südosten&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-150"><strong>*east</strong> finds any string that ends with &quot;east&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-151">*<em>Wert</em>* (Stern)</span><span class="sxs-lookup"><span data-stu-id="11bca-151">*<em>value</em>* (asterisk)</span></span></td>
<td><span data-ttu-id="11bca-152">Enthält den eingegebenen Wert.</span><span class="sxs-lookup"><span data-stu-id="11bca-152">Containing the value that is entered</span></span></td>
<td><span data-ttu-id="11bca-153">Geben Sie einen Stern, den Wert und dann einen weiteren Stern ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-153">Type an asterisk, then a value, and then another asterisk.</span></span></td>
<td><span data-ttu-id="11bca-154"><strong>*st*</strong>  findet alle Zeichenfolgen, die &quot;st&quot; enthalten, wie &quot;Nordosten&quot; und &quot;Südosten&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-154"><strong>*th*</strong> finds any string that contains &quot;th&quot;, such as &quot;Northeast&quot; and &quot;Southeast&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-155">?</span><span class="sxs-lookup"><span data-stu-id="11bca-155">?</span></span> <span data-ttu-id="11bca-156">(Fragezeichen)</span><span class="sxs-lookup"><span data-stu-id="11bca-156">(question mark)</span></span></td>
<td><span data-ttu-id="11bca-157">Enthält ein oder mehrere unbekannte Zeichen.</span><span class="sxs-lookup"><span data-stu-id="11bca-157">Having one or more unknown characters</span></span></td>
<td><span data-ttu-id="11bca-158">Geben Sie an der Position des unbekannten Zeichens im Wert ein Fragezeichen ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-158">Type a question mark at the position of the unknown character in the value.</span></span></td>
<td><span data-ttu-id="11bca-159"><strong>Sm?th</strong> findet das System &quot;Smith&quot; und &quot;Smyth&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-159"><strong>Sm?th</strong> finds &quot;Smith&quot; and &quot;Smyth&quot;.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-160"><em>Wert</em>,<em>Wert</em> (Komma)</span><span class="sxs-lookup"><span data-stu-id="11bca-160"><em>value</em>,<em>value</em> (comma)</span></span></td>
<td><span data-ttu-id="11bca-161">Vergleicht die Werte, die durch Kommas getrennt sind.</span><span class="sxs-lookup"><span data-stu-id="11bca-161">Matching the values that are separated by commas</span></span></td>
<td><span data-ttu-id="11bca-162">Geben Sie alle Kriterien durch Kommas getrennt an.</span><span class="sxs-lookup"><span data-stu-id="11bca-162">Type all your criteria, and separate them by using commas.</span></span></td>
<td><span data-ttu-id="11bca-163"><strong>A, D, F, G</strong> findet genau &quot;A&quot;, &quot;D&quot;, &quot;F&quot; und &quot;G&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-163"><strong>A, D, F, G</strong> finds exactly &quot;A&quot;, &quot;D&quot;, &quot;F&quot;, and &quot;G&quot;.</span></span> <span data-ttu-id="11bca-164"><strong>10, 20, 30, 100</strong> findet genau &quot;10, 20, 30, 100&quot;.</span><span class="sxs-lookup"><span data-stu-id="11bca-164"><strong>10, 20, 30, 100</strong> finds exactly &quot;10, 20, 30, 100&quot;.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-165">(<span class="code">SQL-Anweisung</span>) (SQL-Anweisung in Klammern)</span><span class="sxs-lookup"><span data-stu-id="11bca-165">(<span class="code">SQL statement</span>) (SQL statement between parentheses)</span></span></td>
<td><span data-ttu-id="11bca-166">Übereinstimmung mit einer definierten Abfrage</span><span class="sxs-lookup"><span data-stu-id="11bca-166">Matching a defined query</span></span></td>
<td><span data-ttu-id="11bca-167">Geben Sie eine Abfrage als SQL-Anweisung in Klammern an.</span><span class="sxs-lookup"><span data-stu-id="11bca-167">Type a query as an SQL statement between parentheses.</span></span></td>
<td><span data-ttu-id="11bca-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span><span class="sxs-lookup"><span data-stu-id="11bca-168"><strong><span class="code">(data source.Fieldname != &quot;A&quot;)</span></strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-169">Di</span><span class="sxs-lookup"><span data-stu-id="11bca-169">T</span></span></td>
<td><span data-ttu-id="11bca-170">Datum von heute</span><span class="sxs-lookup"><span data-stu-id="11bca-170">Today's date</span></span></td>
<td><span data-ttu-id="11bca-171">Geben Sie <strong>T</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-171">Type <strong>T</strong>.</span></span></td>
<td><span data-ttu-id="11bca-172"><strong>T</strong> gleicht heutiges Datum ab.</span><span class="sxs-lookup"><span data-stu-id="11bca-172"><strong>T</strong> matches today's date.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-173">(methodName (Parameter)) (<strong>SysQueryRangeUtil</strong>-Methode in Klammern)</span><span class="sxs-lookup"><span data-stu-id="11bca-173">(methodName(parameters)) (<strong>SysQueryRangeUtil</strong> method between parentheses)</span></span></td>
<td><span data-ttu-id="11bca-174">Abgleichen des Werts oder Wertebereichs, der mit den Parametern der <strong>SysQueryRangeUtil</strong>-Methode angegeben wird</span><span class="sxs-lookup"><span data-stu-id="11bca-174">Matching the value or range of values that are specified by the parameters of the <strong>SysQueryRangeUtil</strong> method</span></span></td>
<td><span data-ttu-id="11bca-175">Geben Sie eine <strong>SysQueryRangeUtil</strong>-Methode mit Parametern ein, die den Wert oder Wertebereich angeben.</span><span class="sxs-lookup"><span data-stu-id="11bca-175">Type a <strong>SysQueryRangeUtil</strong> method that has parameters that specify the value or range of values.</span></span></td>
<td><ol>
<li><span data-ttu-id="11bca-176">Klicken Sie auf <strong>Debitoren</strong> &gt; <strong>Rechnungen</strong> &gt; <strong>Offene Debitorenrechnungen</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-176">Click <strong>Accounts receivable</strong> &gt; <strong>Invoices</strong> &gt; <strong>Open customer invoices</strong>.</span></span></li>
<li><span data-ttu-id="11bca-177">Drücken Sie STRG+UMSCHALT+F3, um die Seite <strong>Abfrage</strong> zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="11bca-177">Press Ctrl+Shift+F3 to open the <strong>Inquiry</strong> page.</span></span></li>
<li><span data-ttu-id="11bca-178">Klicken Sie auf der Registerkarte <strong>Bereich</strong> auf <strong>Hinzufügen</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-178">On the <strong>Range</strong> tab, click <strong>Add</strong>.</span></span></li>
<li><span data-ttu-id="11bca-179">Wählen Sie im Feld <strong>Tabelle</strong> die Option <strong>Offene Debitorenbuchungen</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="11bca-179">In the <strong>Table</strong> field, select <strong>Open customer transactions</strong>.</span></span></li>
<li><span data-ttu-id="11bca-180">Wählen Sie im Feld <strong>Feld</strong> <strong>Fälligkeitsdatum</strong> aus.</span><span class="sxs-lookup"><span data-stu-id="11bca-180">In the <strong>Field</strong> field, select <strong>Due date</strong>.</span></span></li>
<li><span data-ttu-id="11bca-181">Geben Sie im Feld <strong>Kriterien</strong> <strong>(yearRange(-2,0))</strong> ein.</span><span class="sxs-lookup"><span data-stu-id="11bca-181">In the <strong>Criteria</strong> field, enter <strong>(yearRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="11bca-182">Klicken Sie auf <strong>OK</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-182">Click <strong>OK</strong>.</span></span> <span data-ttu-id="11bca-183">Die Listenseite wird aktualisiert und listet die Rechnungen auf, die den Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="11bca-183">The list page is updated and lists the invoices that match the criterion that you entered.</span></span> <span data-ttu-id="11bca-184">Bei diesem speziellen Beispiel werden Rechnungen auf der Listenseite aufgeführt, die in den vorherigen zwei Jahren fällig waren.</span><span class="sxs-lookup"><span data-stu-id="11bca-184">For this example, invoices that were due in the previous two years are listed.</span></span></li>
</ol>
<span data-ttu-id="11bca-185">In der Tabelle im nächsten Abschnitt finden Sie zusätzliche Details zu <strong>SysQueryRangeUtil</strong>-Datumsmethoden und einige Beispiele.</span><span class="sxs-lookup"><span data-stu-id="11bca-185">See the table in the next section for additional details about <strong>SysQueryRangeUtil</strong> date methods, and several examples.</span></span></td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a><span data-ttu-id="11bca-186">Erweiterte Datumsabfragen, die SysQueryRangeUtil-Methoden verwenden</span><span class="sxs-lookup"><span data-stu-id="11bca-186">Advanced date queries that use SysQueryRangeUtil methods</span></span>
<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11bca-187">Methode</span><span class="sxs-lookup"><span data-stu-id="11bca-187">Method</span></span></th>
<th><span data-ttu-id="11bca-188">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="11bca-188">Description</span></span></th>
<th><span data-ttu-id="11bca-189">Beispiel</span><span class="sxs-lookup"><span data-stu-id="11bca-189">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="11bca-190">Tag (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="11bca-190">Day (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="11bca-191">Suchen Sie ein Datum im Verhältnis zum Sitzungsdatum.</span><span class="sxs-lookup"><span data-stu-id="11bca-191">Find a date relative to the session date.</span></span> <span data-ttu-id="11bca-192">Positive Werte geben zukünftige Daten an und negative Werte geben ältere Datumsangaben an.</span><span class="sxs-lookup"><span data-stu-id="11bca-192">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="11bca-193"><strong>Morgen</strong> – Eingabe <strong>(Day(1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-193"><strong>Tomorrow</strong> – Enter <strong>(Day(1))</strong>.</span></span></li>
<li><span data-ttu-id="11bca-194"><strong>Heute</strong> – Eingabe <strong>(Day(0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-194"><strong>Today</strong> – Enter <strong>(Day(0))</strong>.</span></span></li>
<li><span data-ttu-id="11bca-195"><strong>Gestern</strong> – Eingabe <strong>(Day(-1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-195"><strong>Yesterday</strong> – Enter <strong>(Day(-1))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span><span class="sxs-lookup"><span data-stu-id="11bca-196">DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</span></span></td>
<td><span data-ttu-id="11bca-197">Suchen Sie einen Datumsbereich im Verhältnis zum Sitzungsdatum.</span><span class="sxs-lookup"><span data-stu-id="11bca-197">Find a range of dates relative to the session date.</span></span> <span data-ttu-id="11bca-198">Positive Werte geben zukünftige Daten an und negative Werte geben ältere Datumsangaben an.</span><span class="sxs-lookup"><span data-stu-id="11bca-198">Positive values indicate future dates, and negative values indicate past dates.</span></span></td>
<td><ul>
<li><span data-ttu-id="11bca-199"><strong>Letzte 30 Tage</strong> – Eingabe <strong>(DayRange(-30,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-199"><strong>Last 30 days</strong> – Enter <strong>(DayRange(-30,0))</strong>.</span></span></li>
<li><span data-ttu-id="11bca-200"><strong>Vorherige 30 Tage und kommende 30 Tage</strong> – Eingabe <strong>(DayRange(-30,30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-200"><strong>Previous 30 days and next 30 days</strong> – Enter <strong>(DayRange(-30,30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="11bca-201">GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="11bca-202">Suchen Sie alle Datumsangaben nach dem angegebenen relativen Datum.</span><span class="sxs-lookup"><span data-stu-id="11bca-202">Find all dates after the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="11bca-203"><strong>Mehr als 30 Tage ab jetzt</strong> – Eingabe <strong>(GreaterThanDate (30))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-203"><strong>More than 30 days from now</strong> – Enter <strong>(GreaterThanDate(30))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-204">GreaterThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="11bca-204">GreaterThanUtcNow ()</span></span></td>
<td><span data-ttu-id="11bca-205">Suchen Sie alle Datums-/Uhrzeiteinträge nach der aktuellen Zeit.</span><span class="sxs-lookup"><span data-stu-id="11bca-205">Find all date/time entries after the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="11bca-206"><strong>Alle zukünftigen Daten/Uhrzeiten</strong> – Eingabe <strong>(GreaterThanUtcNow ())</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-206"><strong>All future date/times</strong> – Enter <strong>(GreaterThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span><span class="sxs-lookup"><span data-stu-id="11bca-207">LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</span></span></td>
<td><span data-ttu-id="11bca-208">Suchen Sie alle Datumsangaben vor dem angegebenen relativen Datum.</span><span class="sxs-lookup"><span data-stu-id="11bca-208">Find all dates before the specified relative date.</span></span></td>
<td><ul>
<li><span data-ttu-id="11bca-209"><strong>Weniger als sieben Tage ab jetzt</strong> – Eingabe <strong>(LessThanDate (7))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-209"><strong>Less than seven days from now</strong> – Enter <strong>(LessThanDate(7))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-210">LessThanUtcNow ()</span><span class="sxs-lookup"><span data-stu-id="11bca-210">LessThanUtcNow ()</span></span></td>
<td><span data-ttu-id="11bca-211">Suchen Sie alle Datums-/Uhrzeiteinträge vor der aktuellen Zeit.</span><span class="sxs-lookup"><span data-stu-id="11bca-211">Find all date/time entries before the current time.</span></span></td>
<td><ul>
<li><span data-ttu-id="11bca-212"><strong>Alle vergangenen Daten/Uhrzeiten</strong> – Eingabe <strong>(LessThanUtcNow ())</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-212"><strong>All past date/times</strong> – Enter <strong>(LessThanUtcNow())</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="11bca-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="11bca-213">MonthRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="11bca-214">Suchen Sie einen Datumsbereich auf Grundlage von Monaten relativ zum aktuellen Monat.</span><span class="sxs-lookup"><span data-stu-id="11bca-214">Find a range of dates, based on months relative to the current month.</span></span></td>
<td><ul>
<li><span data-ttu-id="11bca-215"><strong>Vorherige zwei Monate</strong> – Eingabe <strong>(MonthRange (- 2,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-215"><strong>Previous two months</strong> – Enter <strong>(MonthRange(-2,0))</strong>.</span></span></li>
<li><span data-ttu-id="11bca-216"><strong>Nächste drei Monate</strong> – Eingabe <strong>(MonthRange (0,3))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-216"><strong>Next three months</strong> – Enter <strong>(MonthRange(0,3))</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="11bca-217">YearRange (_relativeFrom=0, _relativeTo=0)</span><span class="sxs-lookup"><span data-stu-id="11bca-217">YearRange (_relativeFrom=0, _relativeTo=0)</span></span></td>
<td><span data-ttu-id="11bca-218">Suchen Sie einen Datumsbereich auf Grundlage von Jahren relativ zum aktuellen Jahr.</span><span class="sxs-lookup"><span data-stu-id="11bca-218">Find a range of dates, based on years relative to the current year.</span></span></td>
<td><ul>
<li><span data-ttu-id="11bca-219"><strong>Nächstes Jahr</strong> – Eingabe <strong>(YearRange (0, 1))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-219"><strong>Next year</strong> – Enter <strong>(YearRange(0, 1))</strong>.</span></span></li>
<li><span data-ttu-id="11bca-220"><strong>Vorheriges Jahr</strong> – Eingabe <strong>(YearRange (-1,0))</strong>.</span><span class="sxs-lookup"><span data-stu-id="11bca-220"><strong>Previous year</strong> – Enter <strong>(YearRange(-1,0))</strong>.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>






