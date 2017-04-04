---
title: "Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen"
description: "In diesem Thema wird die Verwendung von Ausdruckseinschränkungen und Tabelleneinschränkungen beschrieben. Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren. Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten."
author: YuyuScheller
manager: AnnBe
ms.date: 2016-02-24 15 - 08 - 06
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: PCGlobalTableConstraintEdit, PCProductConfigurationModelDetails, PCTableConstraintAttachAttributeTree, PCTableConstraintDefinition
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 53111
ms.assetid: 5c12b1f2-eb89-4648-a755-de412f2eadd6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: f707d45290682e79ee439ba0d504852429defa90
ms.openlocfilehash: 1fe8a0d90a3f707fa7b0fea0310c819ce5040a42
ms.lasthandoff: 03/30/2017


---

# <a name="expression-constraints-and-table-constraints-in-product-configuration-models"></a>Ausdruckseinschränkungen und Tabelleneinschränkungen in Produktkonfigurationsmodellen

In diesem Thema wird die Verwendung von Ausdruckseinschränkungen und Tabelleneinschränkungen beschrieben. Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren. Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten. 

Einschränkungen steuern die Attributwerte, die Sie auswählen können, wenn Sie Produkte für einen Auftrag, ein Verkaufsangebot, eine Bestellung oder einen Produktionsauftrag konfigurieren. Sie können Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten.

## <a name="what-are-expression-constraints"></a>Was sind Ausdruckseinschränkungen?
Ausdruckseinschränkungen werden durch einen Ausdruck bezeichnet, der arithmetische und boolesche Operatoren und Funktionen verwendet. Eine Ausdruckseinschränkung wird für eine bestimmte Komponente in einem Produktkonfigurationsmodell geschrieben. Sie können nicht von einer anderen Komponente wiederverwendet oder für sie freigegeben werden. Die Ausdruckseinschränkungen für eine Komponente können jedoch auf Attribute der Unterkomponenten der Komponente verweisen.

## <a name="what-are-table-constraints"></a>Was sind Tabelleneinschränkungen?
Tabelleneinschränkungen listen die Kombinationen von Werten auf, die für Attribute zulässig sind, wenn Sie ein Produkt konfigurieren. Tabelleneinschränkungsdefinitionen können generisch verwendet werden. Wenn Sie eine Tabelleneinschränkung für eine Komponente in einem Produktkonfigurationsmodell erstellen, wählen Sie eine Tabelleneinschränkungsdefinition aus. Um die Kombinationen zu erstellen, die zulässig sind, fügen Sie Attribute bestimmter Arten den Komponenten hinzu. Jeder Attributtyp hat einen bestimmten Wert.

### <a name="example-of-a-table-constraint"></a>Beispiel einer Tabelleneinschränkung

Dieses Beispiel verdeutlicht, wie Sie die Konfiguration eines Lautsprechers auf bestimmte Gehäuseoberflächen und Frontseiten einschränken können. Die erste Tabelle enthält die Oberflächen und die Frontseiten, die allgemein zur Konfiguration verfügbar sind. Die Werte werden für Gehäuseende ** ** und vorderer ** Grill ** Attributtypen definiert.

| Attributtyp | Werte                      |
|----------------|-----------------------------|
| Gehäuseoberfläche | Schwarz, Eiche, Rosenholz, Weiß |
| Vordergerippe    | Schwarz, Metall, Weiß         |

In der folgenden Tabelle werden die Kombinationen angezeigt, die von der Tabelleneinschränkung **Farbe und Oberfläche** definiert werden. Mithilfe dieser Tabelleneinschränkung können Sie einen Lautsprecher konfigurieren, der ein Eichenoberfläche und einen schwarzen Grill, eine Rosenholzoberfläche und ein weißer Grill usw. hat.

| Fertig stellen         | Grill                       |
|----------------|-----------------------------|
| Eiche            | Schwarz                       |
| Rosenholz       | Weiß                       |
| Weiß          | Schwarz                       |
| Weiß          | Weiß                       |
| Schwarz          | Schwarz                       |
| Schwarz          | Metall                       | 

Sie können die systemdefinierte und benutzerdefinierte Tabelleneinschränkungen erstellen. Weitere Informationen finden Sie unter [Systemdefinierte und benutzerdefinierte Tabelleneinschränkungen](system-defined-user-defined-table-constraints.md).

## <a name="what-syntax-should-be-used-to-write-constraints"></a>Die Syntax verwendet werden soll, um Einschränkungen zu schreiben?
Sie müssen Optimization Modeling Language (OML)-Syntax verwenden, wenn Sie die Einschränkungen schreiben. Das System verwendet Microsoft Foundations-Einschränkungswandler Solver, um die Einschränkungen zu beheben.

## <a name="should-i-use-table-constraints-or-expression-constraints"></a>Soll ich Tabelleneinschränkungen oder Ausdruckseinschränkungen verwenden?
Sie können entweder Ausdruckseinschränkungen oder Tabelleneinschränkungen verwenden, je nachdem, wie Sie die Einschränkungen erstellen möchten. Sie bauen eine Tabelleneinschränkung als Matrix auf, während eine Ausdruckseinschränkung ein einzelner Auszug ist. Wenn Sie ein Produkt konfigurieren, ist es nicht von Bedeutung, welche Art von Einschränkung verwendet wird. Im folgenden Beispiel werden die Unterschiede der zwei zur Verfügung stehenden Optionen veranschaulicht.  

Wenn Sie ein Produkt konfigurieren, indem Sie die folgenden Einschränkungseinstellungen verwenden, sind diese Kombinationen zulässig:

-   Ein Produkt in der Farbe Schwarz und mit Größe 30 oder 50
-   Ein Produkt in der Farbe Rot und mit Größe 20

### <a name="table-constraint-setup"></a>Tabelleneinschränkungseinrichtung

| Farbe | Größe |
|-------|------|
| Schwarz | 30   |
| Schwarz | 50   |
| Rot   | 20   |

### <a name="expression-constraint-setup"></a>Einrichtung von Ausdruckseinschränkungen

(Farbe == "Schwarz" & (Größe == "30" | Größe == "50")) | (Farbe == "Rot" & Größe = "20")

## <a name="should-i-use-operators-or-infix-notation-when-i-write-expression-constraints"></a>Muss ich Operatoren oder Infixschreibweise verwenden, wenn ich Ausdruckseinschränkungen schreibe?
Sie können eine Ausdruckseinschränkung schreiben, indem Sie entweder die verfügbaren Präfixoperatoren oder die Infixschreibweise verwenden. Für die Operatoren **Min**, **Max** und **Abs ** können Sie die Infixschreibweise nicht verwenden. Diese Operatoren sind als Standard in den meisten Programmiersprachen einbezogen.

## <a name="what-operators-and-infix-notation-can-i-use-when-i-write-expression-constraints"></a>Welche Operatoren und Infixschreibweise kann ich verwenden, wenn ich Ausdruckseinschränkungen schreibe?
In den folgenden Tabellen werden die Operatoren und Infixschreibweise aufgelistet, die Sie verwenden können, wenn Sie eine Ausdruckseinschränkung für eine Komponente in einem Produktkonfigurationsmodell schreiben. Den Beispielen in dieser ersten Tabelle können Sie entnehmen, wie Sie einen Ausdruck schreiben, indem Sie entweder Infixschreibweise oder Operatoren verwenden.

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th>Bediener</th>
<th>Beschreibung</th>
<th>Syntax</th>
<th>Beispiele</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Bedeutet</td>
<td>Dies gilt, wenn die erste Bedingung nicht zutrifft, die zweite Bedingung erfüllt wird, oder beide.</td>
<td>Implies[a, b], infix: a -: b</td>
<td><ul>
<li><strong>Operator :</strong> Bedeutet [x! = 0, y &gt;= 0]</li>
<li><strong>Infixschreibweise:</strong> x! = 0 -: y &gt;= 0</li>
</ul></td>
</tr>
<tr class="even">
<td>Und</td>
<td>Dies gilt nur, wenn alle Bedingungen erfüllt sind. Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>Wahr</strong>.</td>
<td>Die args [], Infix: ein &amp; ( &amp; z… &amp;</td>
<td><ul>
<li><strong>Operator :</strong> Die x-== [2], y &lt;= 2</li>
<li><strong>Infixschreibweise:</strong> y &lt;== x 2 &amp; = 2</li>
</ul></td>
</tr>
<tr class="odd">
<td>Oder</td>
<td>Dies trifft zu, wenn jede Bedingung wahr ist. Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>Falsch</strong>.</td>
<td>Oder args [], Infix: a _=_ b _=_ … _=_ z</td>
<td><ul>
<li><strong>Operator :</strong> Oder x-== [2], y &lt;= 2</li>
<li><strong>Infixschreibweise:</strong> x == 2 _=_ y &lt;= 2</li>
</ul></td>
</tr>
<tr class="even">
<td>Plus</td>
<td>Dies summiert die Bedingungen. Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>0</strong>.</td>
<td>Args Plus [], Infix: A + B + + z…</td>
<td><ul>
<li><strong>Operator:</strong> Plus[x, y, 2] == z</li>
<li><strong>Infixschreibweise</strong>: x + y + 2 == z</li>
</ul></td>
</tr>
<tr class="odd">
<td>Minus</td>
<td>Dies negiert das Argument. Dies muss genau eine Bedingung haben.</td>
<td>Minus[expr], Infix: -expr</td>
<td><ul>
<li><strong>Operator:</strong> Minus[x] == y</li>
<li><strong>Infixschreibweise:</strong> -x == y</li>
</ul></td>
</tr>
<tr class="even">
<td>Abs</td>
<td>Dies nimmt den absoluten Wert der Bedingung. Dies muss genau eine Bedingung haben.</td>
<td>Abs[expr]</td>
<td><strong>Operator:</strong> Abs[x]</td>
</tr>
<tr class="odd">
<td>Zeiten</td>
<td>Dies nimmt das Produkt der Bedingungen. Wenn die Anzahl der Bedingungen 0 (Null) ist, ergibt dies <strong>1</strong>.</td>
<td>Args Zeiten [], Infix: B ein * * * z…</td>
<td><ul>
<li><strong>Operator:</strong> Times[x, y, 2] == z</li>
<li><strong>Infixschreibweise</strong>: x * y * 2 == z</li>
</ul></td>
</tr>
<tr class="even">
<td>Antriebskraft</td>
<td>Dies nimmt einen exponentiellen Wert. Dies wendet die Exponenten von rechts nach links an. (Also, ist sie Recht-vereinigend). Daher <strong>Power [A, B, C]</strong> ist zu. <strong>Power</strong> kann nur mit einer positiven Konstante als Exponent verwendet werden.</td>
<td>Leistung args [], Infix: ein ^ B ^… ^ z</td>
<td><ul>
<li><strong>Operator:</strong> Power[x, 2] == y</li>
<li><strong>Infixschreibweise:</strong> x ^ 2 == y</li>
</ul></td>
</tr>
<tr class="odd">
<td>Max.</td>
<td>Dies produziert die umfangreichste Bedingung. Wenn die Anzahl der Bedingungen 0 (Null) ist, produziert dies <strong>Unendlich</strong>.</td>
<td>Max[args]</td>
<td><strong>Operator:</strong> Max[x, y, 2] == z</td>
</tr>
<tr class="even">
<td>Min.</td>
<td>Dies produziert die kleinste Bedingung. Wenn die Anzahl der Bedingungen 0 (Null) ist, produziert dies <strong>Unendlich</strong>.</td>
<td>Min[args]</td>
<td><strong>Operator:</strong> Min[x, y, 2] == z</td>
</tr>
<tr class="odd">
<td>Nicht</td>
<td>Dies produziert die logische Umkehrung der Bedingung. Dies muss genau eine Bedingung haben.</td>
<td>Not[expr], Infix: !expr</td>
<td><ul>
<li><strong>Operator :</strong> Nicht [x nicht y-==] &amp; [3]</li>
<li><strong>Infixschreibweise:</strong> !x!(y == 3)</li>
</ul></td>
</tr>
</tbody>
</table>

Die Beispiele in der nächsten Tabellen zeigen, wie eine Infixnotation geschrieben wird.

| Infixschreibweise    | Beschreibung                                                                                   |
|-------------------|-----------------------------------------------------------------------------------------------|
| x + y + z         | Hinzufügung                                                                                      |
| x \* \* y z       | Multiplikation                                                                                |
| x - y             | Die binäre Subtraktion wird auf die gleiche Weise wie die binäre Addition bei einer negierten Sekunde übersetzt. |
| x ^ y ^ z         | Exponenten mit Rechtsverknüpfung                                                   |
| !x                | Boolesches not                                                                                   |
| x -: y            | Boolesche Auswirkung                                                                           |
|  - | y | z         | Boolesches or                                                                                    |
| x & y & z         | Boolesches and                                                                                   |
| x == y == z       | Gleichheit                                                                                      |
| x != y != z       | Getrennt                                                                                      |
| x &lt; &lt; y z   | Kleiner als                                                                                     |
| x &gt; &gt; y z   | Größer als                                                                                  |
| X &lt;= y &lt;z = | Kleiner oder gleich                                                                         |
| X &gt;= y &gt;z = | Größer oder gleich                                                                      |
| (x)               | Klammern setzten die standardmäßige Rangfolge außer Kraft.                                                      |

## <a name="why-arent-my-expression-constraints-validated-correctly"></a>Warum werden meine Ausdruckseinschränkungen nicht ordnungsgemäß validiert?
Sie können reservierte Schlüsselwörter nicht als Wandlernamen für Attribute, Komponenten oder Unterkomponenten in einem Produktkonfigurationsmodell verwenden. Das hier eine Liste der reservierten Suchbegriffen, die nicht verwendet werden können:

-   Decke
-   Element
-   Gleich
-   Stockwerk
-   Falls
-   Kleiner
-   Größer
-   Bedeutet
-   Protokoll
-   Max.
-   Min.
-   Minus
-   Plus
-   Antriebskraft
-   Zeiten
-   Zeitrahmen
-   Modell
-   Entscheidung
-   Ziel


<a name="see-also"></a>Siehe auch
--------

[Erstellen einer Aufgabenleitfaden " Ausdruckseinschränkung)]http://ax.help.dynamics.com/en/wiki/create-an-expression-constraint/) "

[Fügen Sie eine Berechnung ein Produktkonfigurationsmodell hinzufügen "Aufgabenleitfaden)]http://ax.help.dynamics.com/en/wiki/add-a-calculation-to-a-product-configuration-model/) "


