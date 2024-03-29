---
title: Erweiterte Filter- und Abfragesyntax
description: In diesem Artikel werden die Filter- und Abfrageoptionen für das Dialogfeld „Erweiterter Filter/Sortierung“ und den Übereinstimmungsoperator im Filterbereich oder in den Filtern in den Spaltenüberschriften des Gitters beschrieben.
author: jasongre
ms.date: 03/09/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm
audience: Application User
ms.reviewer: sericks
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89175763357f4309c4eb7874d0068586c5d9e726
ms.sourcegitcommit: 873d66c03a51ecb7082e269f30f5f980ccd9307f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 07/06/2022
ms.locfileid: "9123947"
---
# <a name="advanced-filtering-and-query-syntax"></a>Erweiterter Filter- und Abfragesyntax

[!include [banner](../includes/banner.md)]


[!INCLUDE [PEAP](../../../includes/peap-1.md)]

**Erweiterte Filter- und Abfragesyntax** - In diesem Artikel werden die Filter- und Abfrageoptionen beschrieben, die verfügbar sind, wenn Sie den Operator "entspricht" im Dialogfeld "Erweitertes Filtern/Sortieren" verwenden.

## <a name="advanced-query-syntax"></a>Erweiterte Suchsyntax

<table>
<thead>
<tr>
<th>Syntax</th>
<th>Zeichenbeschreibung</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr>
<td><em>Wert</em></td>
<td>Gleich dem eingegebenen Wert.</td>
<td>Geben Sie den zu suchenden Wert ein.</td>
<td>Mit der Zeichenfolge <strong>Schnepf</strong> wird der Begriff &quot;Schnepf&quot; gefunden.</td>
</tr>
<tr>
<td>!<em>Wert</em> (Ausrufezeichen)</td>
<td>Ungleich dem eingegebenen Wert.</td>
<td>Geben Sie vor dem auszuschließenden Wert ein Ausrufezeichen ein.</td>
<td><strong>!Schnepf</strong> findet alle Werte außer &quot;Schnepf&quot; gefunden.</td>
</tr>
<tr>
<td><em>Von-Wert</em>..<em>Bis-Wert</em> (zwei Punkte)</td>
<td>Zwischen zwei eingegebenen Werten, die von zwei Punkten getrennt werden.</td>
<td>Geben Sie den "Von-Wert", zwei Punkte und dann den "Bis-Wert" ein.</td>
<td><strong>1..10</strong> findet alle Werte von 1 bis 10. In einem Zeichenfolgenfeld findet <strong>A..C</strong> alle Werte, die mit &quot;A&quot; und &quot;B&quot; beginnen, sowie Werte, die genau gleich &quot;C&quot; sind. Diese Abfrage findet beispielsweise nicht &quot;Ca&quot;. Wenn Sie alle Werte von &quot;A<em>&quot; bis &quot;C</em>&quot;, suchen, geben Sie also <strong>A..D</strong> ein.</td>
</tr>
<tr>
<td>..<em>Wert</em> (zwei Punkte)</td>
<td>Kleiner oder gleich dem eingegebenen Wert.</td>
<td>Geben Sie zwei Punkte und dann den Wert ein.</td>
<td><strong>..1000</strong> sucht alle Zahlen, die kleiner oder gleich 1000 sind, wie &quot;100&quot;, &quot;999.95&quot;, und &quot;1,000&quot;.</td>
</tr>
<tr>
<td><em>Wert</em>.. (zwei Punkte)</td>
<td>Größer oder gleich dem eingegebenen Wert.</td>
<td>Geben Sie den Wert und dann zwei Punkte ein.</td>
<td><strong>1000</strong> sucht alle Zahlen, die größer oder gleich 1000 sind, z. B. &quot;1,000&quot;, &quot;1,000.01&quot;, und &quot;1,000,000&quot;.</td>
</tr>
<tr>
<td>&gt;<em>Wert</em> (Zeichen "größer als")</td>
<td>Größer als der eingegebene Wert.</td>
<td>Geben Sie das Zeichen "größer als (<strong>&gt;</strong>) und dann den Wert ein.</td>
<td><strong>&gt;1000</strong> sucht alle Zahlen, die größer als 1000 sind, wie &quot;1000.01&quot;, &quot;20,000&quot;, und &quot;1,000,000&quot;.</td>
</tr>
<tr>
<td>&lt;<em>Wert</em> (Zeichen "kleiner als")</td>
<td>Kleiner als der eingegebene Wert.</td>
<td>Geben Sie das Zeichen "kleiner als (<strong>&lt;</strong>) und dann den Wert ein.</td>
<td><strong>&lt;1000</strong> sucht alle Zahlen, die kleiner als 1000 sind, wie z. B. &quot;999.99&quot;, &quot;1&quot;, und &quot;-200&quot;.</td>
</tr>
<tr>
<td><em>Wert</em>* (Stern)</td>
<td>Beginnend ab dem eingegebenen Wert.</td>
<td>Geben Sie einen Anfangswert und dann einen Stern (<strong>*</strong>) ein.</td>
<td><strong>S*</strong> findet alle Zeichenfolgen, die mit &quot;S&quot; beginnen, wie &quot;Stockholm&quot;, &quot;Sydney&quot;, und &quot;San Francisco&quot;.</td>
</tr>
<tr>
<td>*<em>Wert</em> (Stern)</td>
<td>Endet mit dem eingegebenen Wert.</td>
<td>Geben Sie einen Stern und dann den Endwert ein.</td>
<td><strong>*Osten</strong> findet alle Zeichenfolgen, die auf  &quot;Ostent&quot; enden, wie  &quot;Nordosten&quot; und &quot;Südosten&quot;.</td>
</tr>
<tr>
<td>*<em>Wert</em>* (Stern)</td>
<td>Enthält den eingegebenen Wert.</td>
<td>Geben Sie einen Stern, den Wert und dann einen weiteren Stern ein.</td>
<td><strong>*st*</strong>  findet alle Zeichenfolgen, die &quot;st&quot; enthalten, wie &quot;Nordosten&quot; und &quot;Südosten&quot;.</td>
</tr>
<tr>
<td>? (Fragezeichen)</td>
<td>Enthält ein oder mehrere unbekannte Zeichen.</td>
<td>Geben Sie an der Position des unbekannten Zeichens im Wert ein Fragezeichen ein.</td>
<td><strong>Sm?th</strong> findet das System &quot;Smith&quot; und &quot;Smyth&quot;.</td>
</tr>
<tr>
<td><em>Wert</em>,<em>Wert</em> (Komma)</td>
<td>Vergleicht die Werte, die durch Kommas getrennt sind.</td>
<td>Geben Sie alle Kriterien durch Kommas getrennt an.</td>
<td><strong>A, D, F, G</strong> findet genau &quot;A&quot;, &quot;D&quot;, &quot;F&quot; und &quot;G&quot;. <strong>10, 20, 30, 100</strong> findet genau &quot;10, 20, 30, 100&quot;.</td>
</tr>
<tr>
<td>"" (zwei doppelte Anführungszeichen)</td>
<td>Übereinstimmung mit einem leeren Wert</td>
<td>Geben Sie zwei aufeinanderfolgende doppelte Anführungszeichen ein, um in diesem Feld nach leeren Werten zu filtern.</td>
<td>Zwei aufeinanderfolgende doppelte Anführungszeichen (<strong>""</strong>) finden Zeilen ohne Wert für die aktuelle Spalte.</td>
</tr>
<tr>
<td>(<span class="code">Abfrage von Finanzen und Betrieb</span>) (Finanzen und Betrieb-Abfrage zwischen Klammern)</td>
<td>Übereinstimmung mit einer definierten Abfrage</td>
<td>Geben Sie eine Abfrage als SQL-Anweisung zwischen Klammern ein und verwenden Sie dabei die Abfragesprache für Finanzen und Betrieb.</td>
  <td><strong><span class="code">((AccountNum LIKE "US *") && (DirPartyTable.Name LIKE "Cont*"))</span></strong><br><br> 
       als Syntaxbeispiel für eine Filterbedingung auf ein Feld aus der Stammdatensammlung sowie ein Feld aus einer anderen Datenquelle (für die Seite Alle Kunden)</td>
</tr>
<tr>
<td>Di</td>
<td>Datum von heute</td>
<td>Geben Sie <strong>T</strong> ein.</td>
<td><strong>T</strong> gleicht heutiges Datum ab.</td>
</tr>
<tr>
<td>(methodName (Parameter)) (<strong>SysQueryRangeUtil</strong>-Methode in Klammern)</td>
<td>Abgleichen des Werts oder Wertebereichs, der mit den Parametern der <strong>SysQueryRangeUtil</strong>-Methode angegeben wird</td>
<td>Geben Sie eine <strong>SysQueryRangeUtil</strong>-Methode mit Parametern ein, die den Wert oder Wertebereich angeben.</td>
<td>
<ol>
<li>Klicken Sie auf <strong>Debitoren</strong> &gt; <strong>Rechnungen</strong> &gt; <strong>Offene Debitorenrechnungen</strong>.</li>
<li>Drücken Sie STRG+UMSCHALT+F3, um die Seite <strong>Abfrage</strong> zu öffnen.</li>
<li>Klicken Sie auf der Registerkarte <strong>Bereich</strong> auf <strong>Hinzufügen</strong>.</li>
<li>Wählen Sie im Feld <strong>Tabelle</strong> die Option <strong>Offene Debitorenbuchungen</strong> aus.</li>
<li>Wählen Sie im Feld <strong>Feld</strong> <strong>Fälligkeitsdatum</strong> aus.</li>
<li>Geben Sie im Feld <strong>Kriterien</strong> <strong>(yearRange(-2,0))</strong> ein.</li>
<li>Klicken Sie auf <strong>OK</strong>. Die Listenseite wird aktualisiert und listet die Rechnungen auf, die den Kriterien entsprechen. Bei diesem speziellen Beispiel werden Rechnungen auf der Listenseite aufgeführt, die in den vorherigen zwei Jahren fällig waren.</li>
</ol>
In der Tabelle im nächsten Abschnitt finden Sie zusätzliche Details zu <strong>SysQueryRangeUtil</strong>-Datumsmethoden und einige Beispiele.</td>
</tr>
</tbody>
</table>

## <a name="advanced-date-queries-that-use-sysqueryrangeutil-methods"></a>Erweiterte Datumsabfragen, die SysQueryRangeUtil-Methoden verwenden

<table>
<thead>
<tr>
<th>Methode</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr>
<td>Tag (_relativeDays=0)</td>
<td>Suchen Sie ein Datum im Verhältnis zum Sitzungsdatum. Positive Werte geben zukünftige Daten an und negative Werte geben ältere Datumsangaben an.</td>
<td>
<ul>
<li><strong>Morgen</strong> – Eingabe <strong>(Day(1))</strong>.</li>
<li><strong>Heute</strong> – Eingabe <strong>(Day(0))</strong>.</li>
<li><strong>Gestern</strong> – Eingabe <strong>(Day(-1))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Suchen Sie einen Datumsbereich im Verhältnis zum Sitzungsdatum. Positive Werte geben zukünftige Daten an und negative Werte geben ältere Datumsangaben an.</td>
<td>
<ul>
<li><strong>Letzte 30 Tage</strong> – Eingabe <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Vorherige 30 Tage und kommende 30 Tage</strong> – Eingabe <strong>(DayRange(-30,30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Suchen Sie alle Datumsangaben nach dem angegebenen relativen Datum.</td>
<td>
<ul>
<li><strong>Mehr als 30 Tage ab jetzt</strong> – Eingabe <strong>(GreaterThanDate (30))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>GreaterThanUtcNow ()</td>
<td>Suchen Sie alle Datums-/Uhrzeiteinträge nach der aktuellen Zeit.</td>
<td>
<ul>
<li><strong>Alle zukünftigen Daten/Uhrzeiten</strong> – Eingabe <strong>(GreaterThanUtcNow ())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Suchen Sie alle Datumsangaben vor dem angegebenen relativen Datum.</td>
<td>
<ul>
<li><strong>Weniger als sieben Tage ab jetzt</strong> – Eingabe <strong>(LessThanDate (7))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>LessThanUtcNow ()</td>
<td>Suchen Sie alle Datums-/Uhrzeiteinträge vor der aktuellen Zeit.</td>
<td>
<ul>
<li><strong>Alle vergangenen Daten/Uhrzeiten</strong> – Eingabe <strong>(LessThanUtcNow ())</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Suchen Sie einen Datumsbereich auf Grundlage von Monaten relativ zum aktuellen Monat.</td>
<td>
<ul>
<li><strong>Vorherige zwei Monate</strong> – Eingabe <strong>(MonthRange (- 2,0))</strong>.</li>
<li><strong>Nächste drei Monate</strong> – Eingabe <strong>(MonthRange (0,3))</strong>.</li>
</ul>
</td>
</tr>
<tr>
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Suchen Sie einen Datumsbereich auf Grundlage von Jahren relativ zum aktuellen Jahr.</td>
<td>
<ul>
<li><strong>Nächstes Jahr</strong> – Eingabe <strong>(YearRange (0, 1))</strong>.</li>
<li><strong>Vorheriges Jahr</strong> – Eingabe <strong>(YearRange (-1,0))</strong>.</li>
</ul>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
