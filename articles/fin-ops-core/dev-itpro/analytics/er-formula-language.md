---
title: Formelsprache in der elektronischen Berichterstellung
description: In diesem Thema werden allgemeine Informationen zur Verwendung der Formelsprache bei der elektronischen Berichterstellung bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdd8b9c120fc4a860717a66b9dfa66e6b0daed93
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042710"
---
# <a name="electronic-reporting-formula-language"></a>Formelsprache in der elektronischen Berichterstellung

[!include [banner](../includes/banner.md)]

Die elektronische Berichterstellung (ER) bietet eine leistungsstarke Datenumwandlungserfahrung. Die Sprache, in der die erforderlichen Datenmanipulationen im ER-Formeldesigner ausgedrückt werden, ähnelt der Formelsprache in Microsoft Excel.

## <a name="basic-syntax"></a>Grundlegende Syntax

Er-Ausdrücke können einzelne oder alle folgenden Elemente enthalten:

- [Konstanten](#Constants)
- [Operatoren](#Operators)
- [Verweise](#References)
- [Pfade](#Paths)
- [Funktionen](#Functions)

## <a name="Constants">Konstanten</a>

Wenn Sie Ausdrücke entwerfen, können Sie Text und numerische Konstanten (das heißt Werte, die nicht berechnet werden) verwenden. So wird beispielsweise der Ausdruck `VALUE ("100") + 20` als numerische Konstante **20** verwendet und die Zeichenfolgenkonstante **"100"** gibt den numerischen Wert **120** zurück.

Der EB-Formeldesigner unterstützt Escapesequenzen. Daher können Sie eine Ausdruckszeichenfolge angeben, die anders behandelt werden soll. Beispielsweise gibt der Ausdruck `"Leo Tolstoy ""War and Peace"" Volume 1"` die Textzeichenfolge **Leo Tolstoy "War and Peace" Volume 1** zurück.

## <a name="Operators">Operatoren</a>

Die folgende Tabelle zeigt die arithmetischen Operatoren, die Sie verwenden können, um grundlegende mathematische Arbeitsgänge auszuführen, wie Addition, Subtraktion, Multiplikation und Division.

| Bediener | Dies bedeutet               | Beispiel     |
|----------|-----------------------|-------------|
| +        | Hinzufügung              | `1+2`       |
| -        | Subtraktion, Negation | `5-2`, `-1` |
| \*       | Multiplikation        | `7\*8`      |
| /        | Geschäftsbereich              | `9/3`       |

In der folgenden Tabelle werden die Vergleichsoperatoren angezeigt, die unterstützt werden. Sie können diese Operatoren verwenden, um zwei Werte zu vergleichen.

| Bediener | Dies bedeutet                  | Beispiel      |
|----------|--------------------------|--------------|
| =        | Gleich                    | `X=Y`        |
| &gt;     | Größer als             | `X>Y`        |
| &lt;     | Kleiner als                | `X<Y`        |
| &gt;=    | Größer oder gleich | `X>=Y`       |
| &lt;=    | Kleiner oder gleich    | `X<=Y`       |
| &lt;&gt; | Ungleich             | `X<>Y`       |

Darüber hinaus können Sie auch ein kaufmännisches Und-Zeichen (&) als Textverkettungsoperator verwenden. Auf diese Weise können Sie eine oder mehrere Textzeichenfolgen zu einem einzigen Stück Text verbinden oder verketten.

| Bediener | Dies bedeutet     | Beispiel                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Verketten | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Vorrangigkeit

Die Reihenfolge, in der die Teile eines zusammengesetzten Ausdrucks ausgewertet werden, ist wichtig. Beispielsweise variiert das Ergebnis des Ausdrucks `1 + 4 / 2` , je nachdem, ob der Additionsvorgang oder der Divisionsvorgang zuerst erfolgt. Sie können Klammern verwenden, um explizit zu definieren, wie ein Ausdruck ausgewertet werden soll. Um beispielsweise anzugeben, dass die Addition zuerst ausgeführt werden soll, können Sie den vorhergehenden Ausdruck in `(1 + 4) / 2` ändern. Wenn Sie die Reihenfolge der Vorgänge, die in einem Ausdruck ausgeführt werden müssen, nicht explizit angeben, basiert die Reihenfolge auf der standardmäßigen Prioritätsreihenfolge, die den unterstützten Operatoren zugewiesen ist. Die folgende Tabelle zeigt die Prioritätsreihenfolge an, die jedem Operator zugewiesen ist. Operatoren, die eine höhere Rangfolge haben, (beispielsweise 7), werden vor Operatoren ausgewertet, die eine niedrigere Rangfolge haben, (beispielsweise 1).

| Priorität | Operatoren      | Syntax                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Gruppieren       | ( … )                                                                   |
| 6          | Mitgliedszugriff  | … . …                                                                   |
| 5          | Funktionsaufrufe  | … ( … )                                                                 |
| 4          | Multiplikation | … \* …<br>… / …                                                         |
| 3          | Ergänzung       | … + …<br>… - …                                                          |
| 2          | Vergleich     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Trennung     | … , …                                                                   |

Wenn ein Ausdruck mehrere aufeinander folgende Operatoren enthält, die dieselbe Rangfolge haben, werden diese Arbeitsgänge von links nach rechts ausgewertet. Beispielsweise gibt der Ausdruck `1 + 6 / 2 \* 3 > 5` **true** zurück. Es wird empfohlen, dass Sie Klammern verwenden, um die gewünschte Reihenfolge der Arbeitsgänge für Ausdrucke explizit anzugeben, damit Ausdrücke besser lesbar und verwaltbar sind.

## <a name="References">Verweise</a>

Alle Datenquellen der aktuellen EB-Komponente, die während des Entwurfs eines Ausdrucks verfügbar sind, können als benannte Referenzen verwendet werden. Die aktuelle ER-Komponente kann entweder eine Modellzuordnung oder ein Format sein. Zum Beispiel beinhaltet die aktuelle ER-Datenmodellzuordnung die Datenquelle **ReportingDate**, die den Wert des Datentyps *DateTime* zurückgibt. Um diesen Wert im generierenden Dokument korrekt zu formatieren, können Sie auf die Datenquelle im Ausdruck als `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")` verweisen.

Allen Zeichen im Namen einer verweisenden Datenquelle, die keinen Buchstaben des Alphabets darstellen, muss ein einfaches Anführungszeichen (') vorausgehen. Wenn der Name einer verweisenden Datenquelle, der mindestens ein Symbol enthält, das keinen Buchstaben des Alphabets darstellt, muss der Name in einfache Anführungszeichen gesetzt werden. Diese nichtalphabetischen Symbole können Satzzeichen oder andere geschriebene Symbole sein. Im Folgenden finden Sie einige Beispiele hierfür:

- Auf die Datenquelle **Aktuelles Datum und Zeit** muss in einem EB-Ausdruck als `'Today''s date & time'` verwiesen werden.
- Auf die Methode **name()** der Datenquelle **Kunden** muss in einem EB-Ausdruck als `Customers.'name()'` verwiesen werden.

Wenn die Methoden der Anwendungsdatenquellen Parameter besitzen, wird der folgende Syntax verwendet, um diese Methoden aufzurufen:

- Wenn die Methode **isLanguageRTL** der Datenquelle **System** einen Parameter **EN-US** des Datentyps *Zeichenfolge* hat, muss auf diese Methode in einem EB-Ausdruck als `System.isLanguageRTL("EN-US")` verwiesen werden.
- Anführungszeichen sind nicht erforderlich, wenn ein Methodenname nur alphanumerische Symbole enthält. Sie sind jedoch für eine Methode einer Tabelle erforderlich, wenn der Name Klammern enthält.

Wenn die Datenquelle **System** einer EB-Zuordnung hinzugefügt wird, die auf die Anwendungsklasse **Global** verweist, gibt der Ausdruck `System.isLanguageRTL("EN-US ")` den *booleschen* Wert **FALSE** zurück. Der geänderte Ausdruck `System.isLanguageRTL("AR")` gibt den *booleschen* Wert **TRUE** zurück.

Sie können die Art und Weise eingrenzen, in der Werte an die Parameter dieses Methodentyps übergeben werden:

- Nur Konstanten können an andere Methoden dieses Typs übergeben werden. Die Werte der Konstanten werden zur Entwurfszeit definiert.
- Nur primitive (grundlegende) Datentypen werden für Parameter dieses Typs unterstützt. Die primitiven Datentypen umfassen *ganze Zahlen*, *tatsächlich*, *boolesch* und *Zeichenfolge*.

## <a name="Paths">Pfade</a>

Wenn ein Ausdruck auf eine strukturierte Datenquelle verweist, können Sie die Pfadbeschreibung verwenden, um ein bestimmtes primitives Element dieser Datenquelle auszuwählen. Ein Punktzeichen (. ) wird verwendet, um einzelne Elemente einer strukturierten Datenquelle zu unterteilen. Zum Beispiel enthält die aktuelle EB-Datenmodellzuordnung die Datenquelle **InvoiceTransactions**, und diese Datenquelle gibt eine Liste von Datensätzen zurück. Die **InvoiceTransactions**-Datensatzstruktur enthält die Felder **AmountDebit** und **AmountCredit**, und diese beiden Felder geben numerische Werte zurück. Daher können Sie den folgenden Ausdruck entwerfen, um den Rechnungsbetrag zu berechnen: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Die `InvoiceTransactions.AmountDebit`-Konstruktion in diesem Ausdruck ist der Pfad, der für den Zugriff auf das Feld **AmountDebit** der Datenquelle **InvoiceTransactions** des Typs *Datensatzliste* verwendet wird.

### <a name="relative-path"></a>Relativer Pfad

Wenn der Pfad einer strukturierten Datenquelle mit einem „at“ -Zeichen (@) beginnt, handelt es sich um einen relativen Pfad. Das „at“ -Zeichen wird anstelle des verbleibenden Teils des absoluten Pfads der verwendeten hierarchischen Baumstruktur angezeigt. Die folgende Abbildung zeigt ein Beispiel. Hier gibt der absolute Pfad `Ledger.'accountingCurrency()'` an, dass der Buchhaltungswährungswert aus der Datenquelle **Sachkonto** im Feld **AccountingCurrency** des Datenmodells eingetragen ist.

![Beispiel für einen absoluten Pfad auf der Designer-Seite für ER-Modellzuordnungen](./media/ER-FormulaLanguage-AbsolutePath.png)

Das Beispiel in der folgenden Abbildung zeigt, wie ein relativer Pfad verwendet wird. Der relative Pfad `@.AccountNum` zeigt an, dass das Feld **AccountNum** der Datenquelle **Intrastat** (die eine Ebene über dem Feld **AccountNum** im hierarchischen Baum des Datenmodells erscheint) verwendet wird, um die Debitoren- oder Kreditorenkontonummer in das Feld **AccountNum** des Datenmodells einzugeben.

![Beispiel für einen relativen Pfad auf der Designer-Seite für ER-Modellzuordnungen](./media/ER-FormulaLanguage-RelativePath1.png)

Der verbleibende Teil des absoluten Pfades wird auch im [ER Formeleditor](general-electronic-reporting-formula-designer.md) angezeigt.

![Verbleibender Teil des absoluten Pfads auf der Designer-Seite für ER-Formeln](./media/ER-FormulaLanguage-RelativePath2.png)

## <a name="Functions">Funktionen</a>

Integrierte ER-Funktionen können in ER-Ausdrücken verwendet werden. Alle Datenquellen des Ausdruckskontexts (die aktuelle EB-Modellzuordnung oder das EB-Format) können als Parameter von aufrufenden Funktionen in Übereinstimmung mit der Liste von Argumenten zum Aufrufen von Funktionen verwendet werden. Konstanten können auch als Parameter aufrufender Funktionen verwendet werden. Zum Beispiel enthält die aktuelle EB-Datenmodellzuordnung die Datenquelle **InvoiceTransactions**, und diese Datenquelle gibt eine Liste von Datensätzen zurück. Die **InvoiceTransactions**-Datensatzstruktur enthält die Felder **AmountDebit** und **AmountCredit**, und diese beiden Felder geben numerische Werte zurück. Um daher den Rechnungsbetrag zu berechnen, können Sie den folgenden Ausdruck entwerfen, der die integrierte EB-Rundungsfunktion verwendet: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Beim Entwerfen von ER-Modellzuordnungen und ER-Berichten können Sie ER-Funktionen aus den folgenden Kategorien verwenden:

- [Datums- und Zeitfunktionen](er-functions-category-datetime.md)
- [Listenfunktionen](er-functions-category-list.md)
- [Logische Funktionen](er-functions-category-logical.md)
- [Rechenoperationen](er-functions-category-mathematical.md)
- [Datensatzfunktionen](er-functions-category-record.md)
- [Textfunktionen](er-functions-category-text.md)
- [Datensammlungsfunktionen](er-functions-category-data-collection.md)
- [Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)
- [Funktionen zur Typenumrechnung](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Listenerweiterung der Funktionen

ER ermöglicht es Ihnen, die Liste von Funktionen zu verlängern, die in ER-Ausdrücken verwendet werden. Etwas technischer Aufwand ist erforderlich. Detaillierte Informationen finden Sie unter [Erweitern Sie die Liste der Funktionen der elektronischen Berichterstattung (ER)](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Zusammengesetzte Ausdrücke

Sie können zusammengesetzte Ausdrücke erstellen, die Funktionen aus verschiedenen Kategorien verwenden, sofern die Datentypen übereinstimmen. Wenn Sie Funktionen zusammen verwenden, passen Sie den Datentyp der Ausgabe von einer Funktion an den Eingabedatentyp an, der von einer anderen Funktion benötigt wird. Um beispielsweise einen möglichen „list-is-empty“-Fehler bei der Bindung eines Feldes mit dem EB-Formatelement zu vermeiden, kombinieren Sie Funktionen aus der Kategorie [List](er-functions-category-list.md) mit einer Funktion aus der Kategorie [Logical](er-functions-category-logical.md), wie das folgende Beispiel zeigt. Hier verwendet die Formel die [IF](er-functions-logical-if.md)-Funktion, um zu testen, ob die **IntrastatTotals**-Liste leer ist, bevor der Wert der erforderlichen Aggregation aus dieser Liste zurückgegeben wird. Wenn die **IntrastatTotals**-Liste leer ist, gibt die Formel **0** (Null) zurück.

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Mehrere Lösungen

Häufig können Sie dasselbe Datenumwandlungsergebnis auf verschiedene Arten erhalten, indem Sie Funktionen aus verschiedenen Kategorien oder verschiedene Funktionen aus derselben Kategorie verwenden. Beispielsweise kann der vorherige Ausdruck auch mithilfe der [COUNT](er-functions-list-count.md)-Funktion aus der [List](er-functions-category-list.md)-Kategorie konfiguriert werden.

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Überblick über die elektronische Berichterstellung](general-electronic-reporting.md)

[Formeldesigner in der elektronischen Berichterstellung](general-electronic-reporting-formula-designer.md)

[Die Liste der elektronischen Berichterstellungsfunktionen erweitern](general-electronic-reporting-formulas-list-extension.md)
