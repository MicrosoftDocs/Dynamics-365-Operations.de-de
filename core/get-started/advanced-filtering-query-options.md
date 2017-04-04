---
title: "Erweiterte und Abfragensyntax gewünschten"
description: "In diesem Artikel werden die Filter- und Abfrageoptionen beschrieben, die verfügbar sind, wenn Sie den &quot;entspricht&quot;-Operator im Dialogfeld &quot;Erweitertes Filtern/Sortieren&quot; verwenden."
author: jasongre
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: SysQueryForm
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 3811
ms.assetid: b4969b30-2fe1-4a3c-bbea-725dc37c8b60
ms.search.region: Global
ms.author: jasongre
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: 5ee7a04572e350a7c08d0418bade6d332aa920c6
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-filtering-and-query-syntax"></a>Erweiterte und Abfragensyntax gewünschten

In diesem Artikel werden die Filter- und Abfrageoptionen beschrieben, die verfügbar sind, wenn Sie den "entspricht"-Operator im Dialogfeld "Erweitertes Filtern/Sortieren" verwenden.

<a name="advanced-query-syntax"></a>Erweiterte Abfragensyntax
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
<th>Syntax</th>
<th>Zeichenbeschreibung</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><em>Wert</em></td>
<td>Gleich dem eingegebenen Wert.</td>
<td>Geben Sie den zu suchenden Wert ein.</td>
<td><strong>Smith</strong> Suchen &quot;Smith&quot;.</td>
</tr>
<tr class="even">
<td>Mit "!<em>Wert</em> Ausrufezeichen ()</td>
<td>Ungleich dem eingegebenen Wert.</td>
<td>Geben Sie vor dem auszuschließenden Wert ein Ausrufezeichen ein.</td>
<td><strong>Mit "! Smith</strong> sucht alle Werte außer Smith &quot;.</td>
</tr>
<tr class="odd">
<td><em>Von-Wert</em>..<em>Bis-Wert</em> (zwei Punkte)</td>
<td>Zwischen zwei eingegebenen Werten, die von zwei Punkten getrennt werden.</td>
<td>Geben Sie den "Von-Wert", zwei Punkte und dann den "Bis-Wert" ein.</td>
<td><strong>1..10</strong> sucht alle Werte von 1 bis 10. In einem Zeichenfolgefeld findet, <strong>A.C</strong> sucht alle Werte, die mit " A und &quot; B &quot;,&quot;und beginnen &quot;Werte, die genau gleich C. &quot;z&quot;sind diese Abfrage, CA &quot;nicht finden.&quot; Wenn Sie alle Werte von &quot; " A* &quot;C* &quot;suchen&quot;, eingeben <strong>A.D "</strong>.</td>
</tr>
<tr class="even">
<td>..<em>Wert</em> (zwei Punkte)</td>
<td>Kleiner oder gleich dem eingegebenen Wert.</td>
<td>Geben Sie zwei Punkte und dann den Wert ein.</td>
<td><strong>. .1000</strong> sucht alle, die kleiner oder gleich 1000 sind, z 100 &quot;,&quot;ist &quot;999.95&quot;, und &quot;1.000&quot;.</td>
</tr>
<tr class="odd">
<td><em>Wert</em>.. (zwei Punkte)</td>
<td>Größer oder gleich dem eingegebenen Wert.</td>
<td>Geben Sie den Wert und dann zwei Punkte ein.</td>
<td><strong>1000..</strong> sucht alle, die größer oder gleich 1000 sind, z 1.000 &quot;,&quot;1.000,01 &quot;, 1.000.000&quot;und &quot;.</td>
</tr>
<tr class="even">
<td>&gt;<em>Wert</em> (Größer-als-Zeichen)</td>
<td>Größer als der eingegebene Wert.</td>
<td>Geben Sie einen Größer-als-Zeichen (<strong>&gt;</strong>) und dann den Wert ein.</td>
<td><strong>&gt;1000</strong> sucht alle, die größer als 1000 sind, z, &quot;1000.01&quot;20.000 &quot;&quot;und 1.000.000 &quot;beträgt&quot;.</td>
</tr>
<tr class="odd">
<td>&lt;<em>Wert</em> (Kleiner-als-Zeichen)</td>
<td>Kleiner als der eingegebene Wert.</td>
<td>Geben Sie einen Kleiner-als-Zeichen (<strong>&lt;</strong>) und dann den Wert ein.</td>
<td><strong>&lt;1000</strong> sucht alle, die kleiner als 1000 sind, z, &quot;999.99&quot;1 &quot;&quot;und -200 &quot;beträgt&quot;.</td>
</tr>
<tr class="even">
<td><em>Wert</em>* Sternchen ()</td>
<td>Beginnend ab dem eingegebenen Wert.</td>
<td>Geben Sie einen Anfangswert und dann einen Stern ein (<strong>*</strong>).</td>
<td><strong>Mit " S*</strong> gesucht, die mit " &quot;S,&quot;z Stockholm &quot;,&quot;Sydney &quot;&quot;und San &quot;Francisco beginnt&quot;.</td>
</tr>
<tr class="odd">
<td>*<em>value</em> (asterisk)</td>
<td>Endet mit dem eingegebenen Wert.</td>
<td>Geben Sie einen Stern und dann den Endwert ein.</td>
<td><strong>*osten</strong> gesucht, die mit " &quot;Ost " Nordosten &quot;Südosten &quot;,&quot;wie und&quot; beendet&quot;.</td>
</tr>
<tr class="even">
<td>*<em>Wert</em>* Sternchen ()</td>
<td>Enthält den eingegebenen Wert.</td>
<td>Geben Sie einen Stern, den Wert und dann einen weiteren Stern ein.</td>
<td><strong>*st</strong> gesucht &quot;, die enthält&quot;, z Nordosten&quot; Südosten&quot;und &quot;.</td>
</tr>
<tr class="odd">
<td>? (Fragezeichen)</td>
<td>Enthält ein oder mehrere unbekannte Zeichen.</td>
<td>Geben Sie an der Position des unbekannten Zeichens im Wert ein Fragezeichen ein.</td>
<td><strong>Inspektion?</strong> Suchen &quot;Smith&quot; Smyth&quot;und &quot;.</td>
</tr>
<tr class="even">
<td><em>Wert</em>,<em>Wert</em> (Komma)</td>
<td>Vergleicht die Werte, die durch Kommas getrennt sind.</td>
<td>Geben Sie alle Kriterien durch Kommas getrennt an.</td>
<td><strong>A, D, F, G</strong> findet &quot;das System genau "&quot;A ", &quot;D-&quot;, &quot;und &quot;F-&quot;G&quot;<strong>10, 20, 30, 100</strong> . -Suchen genau 10,20,30,100&quot;.</td>
</tr>
<tr class="odd">
<td>(<span class="code">SQL-Anweisung</span>) (SQL-Anweisung in Klammern)</td>
<td>Übereinstimmung mit einer definierten Abfrage</td>
<td>Geben Sie eine Abfrage als SQL-Anweisung in Klammern an.</td>
<td><strong><span class="code">(Datenquelle. Feldname! = &quot;A&quot;)</span></strong></td>
</tr>
<tr class="even">
<td>Di</td>
<td>Datum von heute</td>
<td>Geben Sie <strong>T</strong> ein.</td>
<td><strong>T</strong> gleicht heutiges Datum ab.</td>
</tr>
<tr class="odd">
<td>(methodName (Parameter)) (<strong>SysQueryRangeUtil</strong>-Methode in Klammern)</td>
<td>Abgleichen des Werts oder Wertebereichs, der mit den Parametern der <strong>SysQueryRangeUtil</strong>-Methode angegeben wird</td>
<td>Geben Sie eine <strong>SysQueryRangeUtil</strong>-Methode mit Parametern ein, die den Wert oder Wertebereich angeben.</td>
<td><ol>
<li>Klicken <strong>Debitoren</strong> &gt; <strong>Rechnungen</strong> &gt; <strong>Offene Debitorenrechnungen</strong> Sie auf.</li>
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
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>Methode</th>
<th>Beschreibung</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Tag (_relativeDays=0)</td>
<td>Suchen Sie ein Datum im Verhältnis zum Sitzungsdatum. Positive Werte geben zukünftige Daten an und negative Werte geben ältere Datumsangaben an.</td>
<td><ul>
<li><strong>Morgen</strong> – Eingabe <strong>(Day(1))</strong>.</li>
<li><strong>Heute</strong> – Eingabe <strong>(Day(0))</strong>.</li>
<li><strong>Gestern</strong> – Eingabe <strong>(Day(-1))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>DayRange (_relativeDaysFrom=0, _relativeDaysTo=0)</td>
<td>Suchen Sie einen Datumsbereich im Verhältnis zum Sitzungsdatum. Positive Werte geben zukünftige Daten an und negative Werte geben ältere Datumsangaben an.</td>
<td><ul>
<li><strong>Letzte 30 Tage</strong> – Eingabe <strong>(DayRange(-30,0))</strong>.</li>
<li><strong>Vorherige 30 Tage und kommende 30 Tage</strong> – Eingabe <strong>(DayRange(-30,30))</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>GreaterThanDate (_relativeDays=0) GreaterThanUtcDate (_relativeDays=0)</td>
<td>Suchen Sie alle Datumsangaben nach dem angegebenen relativen Datum.</td>
<td><ul>
<li><strong>Mehr als 30 Tage ab jetzt</strong> – Eingabe <strong>(GreaterThanDate (30))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>GreaterThanUtcNow ()</td>
<td>Suchen Sie alle Datums-/Uhrzeiteinträge nach der aktuellen Zeit.</td>
<td><ul>
<li><strong>Alle zukünftigen Daten/Uhrzeiten</strong> – Eingabe <strong>(GreaterThanUtcNow ())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>LessThanDate (_relativeDays=0) LessThanUtcDate (_relativeDays=0)</td>
<td>Suchen Sie alle Datumsangaben vor dem angegebenen relativen Datum.</td>
<td><ul>
<li><strong>Weniger als sieben Tage ab jetzt</strong> – Eingabe <strong>(LessThanDate (7))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>LessThanUtcNow ()</td>
<td>Suchen Sie alle Datums-/Uhrzeiteinträge vor der aktuellen Zeit.</td>
<td><ul>
<li><strong>Alle vergangenen Daten/Uhrzeiten</strong> – Eingabe <strong>(LessThanUtcNow ())</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MonthRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Suchen Sie einen Datumsbereich auf Grundlage von Monaten relativ zum aktuellen Monat.</td>
<td><ul>
<li><strong>Vorherige zwei Monate</strong> – Eingabe <strong>(MonthRange (- 2,0))</strong>.</li>
<li><strong>Nächste drei Monate</strong> – Eingabe <strong>(MonthRange (0,3))</strong>.</li>
</ul></td>
</tr>
<tr class="even">
<td>YearRange (_relativeFrom=0, _relativeTo=0)</td>
<td>Suchen Sie einen Datumsbereich auf Grundlage von Jahren relativ zum aktuellen Jahr.</td>
<td><ul>
<li><strong>Nächstes Jahr</strong> – Eingabe <strong>(YearRange (0, 1))</strong>.</li>
<li><strong>Vorheriges Jahr</strong> – Eingabe <strong>(YearRange (-1,0))</strong>.</li>
</ul></td>
</tr>
</tbody>
</table>




