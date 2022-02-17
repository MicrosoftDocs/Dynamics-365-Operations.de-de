---
title: ORDERBY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ORDERBY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 963d55bcf98a9109c8b6ceb57edf5b55f15a2b0f
ms.sourcegitcommit: 89655f832e722cefbf796a95db10c25784cc2e8e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/31/2022
ms.locfileid: "8075173"
---
# <a name="orderby-er-function"></a>ORDERBY EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ORDERBY` gibt die angegebene Liste mit dem Wert *Datensatzliste* zurück, nachdem sie nach den angegebenen Argumenten sortiert wurde. Diese Argumente können als Ausdrücke definiert werden.

## <a name="syntax-1"></a><a name="syntax-1"></a>Syntax 1

```vb
ORDERBY (list, expression 1[, expression 2, …, expression N])
```

## <a name="syntax-2"></a><a name="syntax-2"></a>Syntax 2

```vb
ORDERBY (location, list, expression 1[, expression 2, …, expression N])
```

> [!NOTE]
> Diese Syntax wird für Microsoft Dynamics 365 Finance Version 10.0.25 und höher unterstützt.

## <a name="arguments"></a>Argumente

`location`: *[String](er-formula-supported-data-types-primitive.md#string)*

Der Ort, an dem die Sortierung ausgeführt werden soll. Die folgenden Optionen sind gültig:

- "Query"
- "InMemory"

`list`: *[Datensatzliste](er-formula-supported-data-types-composite.md#record-list)*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`expression 1`: *Feld*

Der gültige Pfad eines Feldes der Datenquelle, die durch das Argument `list` der aufgerufenen Funktion referenziert wird. Das referenzierte Feld muss ein Feld des primitiven Datentyps sein. Dieses Argument ist erforderlich.

`expression N`: *Feld*

Der gültige Pfad eines Feldes der Datenquelle, die durch das Argument `list` der aufgerufenen Funktion referenziert wird. Das referenzierte Feld muss ein Feld des primitiven Datentyps sein. Diese zusätzlichen Argumente sind optional.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

### <a name="syntax-1"></a>Syntax 1

Die Datensortierung wird immer im Speicher des Anwendungsservers durchgeführt. Weitere Einzelheiten finden Sie unter [Beispiel 1](#example-1).

### <a name="syntax-2"></a>Syntax 2

### <a name="sorting-in-memory"></a>Sortieren im Speicher

Wenn das Argument `location` als **InMemory** angegeben wird, erfolgt die Datensortierung im Speicher eines Anwendungsservers. Weitere Einzelheiten finden Sie unter [Beispiel 2](#example-2).

### <a name="sorting-in-database"></a>Sortieren in der Datenbank

Wenn das Argument `location` als **Abfrage** angegeben wird, erfolgt die Sortierung der Daten auf Datenbankebene. In diesem Fall muss das Argument `list` auf eine der folgenden [Electronic reporting (ER)](general-electronic-reporting.md) Datenquellen zeigen, die die Anwendungsquelle angibt, für die eine direkte Datenbankabfrage eingerichtet werden kann:

- Data source vom Typ *Tabellendatensätze*
- Relation einer Datenquelle vom Typ *Tabellendatensätze*
- Datenquelle vom Typ *Berechnungsfeld*

Die Argumente `expression 1` und `expression N` müssen auf Felder einer ER-Datenquelle zeigen, die die entsprechenden Felder der Anwendungsquelle angibt, für die auch eine direkte Datenbankabfrage eingerichtet werden kann.

Wenn eine direkte Datenbankabfrage nicht möglich ist, wird im Designer für die Zuordnung von ER-Modellen ein [Fehler](er-components-inspections.md#i18) angezeigt. Die Nachricht, die Sie erhalten, besagt, dass der EB-Ausdruck, der die `ORDERBY`-Funktion enthält, nicht zur Laufzeit ausgeführt werden kann.

Um eine bessere Leistung zu erzielen, empfehlen wir Ihnen, die Option **Abfrage** zu verwenden, wenn die Sortierung für Anwendungsdatenquellen konfiguriert ist, die eine große Anzahl von Datensätzen enthalten können (z.B. für transaktionale Anwendungstabellen).

> [!NOTE]
> Die Funktion `ORDEBY` selbst kann nicht in eine direkte Datenbankabfrage übersetzt werden. Daher ist eine ER-Datenquelle, die diese Funktion enthält, nicht abfragbar. Es kann auch nicht im Rahmen von ER-Funktionen wie [FILTER](er-functions-list-filter.md) und [ALLITEMSQUERY](er-functions-list-allitemsquery.md) verwendet werden, wo nur abfragbare Datenquellen verwendet werden können.

Weitere Einzelheiten finden Sie unter [Beispiel 3](#example-3) und [Beispiel 4](#example-4).

### <a name="comparability"></a>Vergleichbarkeit

Da die SQL-Datenbank-Engine und der Finance-Anwendungsserver einen unterschiedlichen Ranking-Wert für ein einzelnes Zeichen verwenden können, kann das Sortierergebnis derselben Liste von Datensätzen unterschiedlich ausfallen, wenn ein [String](er-formula-supported-data-types-primitive.md#string)-Feld für die Sortierung verwendet wird. Weitere Details finden Sie unter [Beispiel 5](#example-5).

## <a name="example-1-in-memory-default-execution"></a><a name="example-1"></a>Beispiel 1: In-Memory-Standardausführung

Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("C|B|A", "|")` enthält, gibt der Ausdruck `FIRST( ORDERBY( DS, DS. Value)).Value` den Textwert **"A"** zurück.

## <a name="example-2-in-memory-explicit-execution"></a><a name="example-2"></a>Beispiel 2: Explizite speicherinterne Ausführung

Wenn **Kreditor** als ER-Datenquelle vom Typ *Tabellendatensätze* konfiguriert ist, die auf die Tabelle **VendTable** verweist, geben sowohl der Ausdruck `ORDERBY (Vendor, Vendor.'name()')` als auch der Ausdruck `ORDERBY ("InMemory", Vendor, Vendor.'name()')` eine Liste von Kreditoren zurück, die in aufsteigender Reihenfolge nach Namen sortiert ist.

Wenn Sie den Ausdruck `ORDERBY ("Query", Vendor, Vendor.'name()')` im Designer für die Zuordnung von ER-Modellen konfigurieren, kommt es zur Entwurfszeit zu einem Validierungsfehler [Fehler](er-components-inspections.md#i8), weil der Pfad `Vendor.'name()'` auf eine Anwendungsmethode verweist, deren Logik nicht in eine direkte Datenbankabfrage übersetzt werden kann.

## <a name="example-3-database-query"></a><a name="example-3"></a>Beispiel 3: Datenbankabfrage

Wenn **TaxTransaction** als ER-Datenquelle vom Typ *Tabellendatensätze* konfiguriert ist, die auf die Tabelle **TaxTrans** verweist, sortiert der Ausdruck `ORDERBY ("Query", TaxTransaction, TaxTransaction.TaxCode)` Datensätze auf der Ebene der Anwendungsdatenbank und gibt eine Liste von Steuertransaktionen zurück, die in aufsteigender Reihenfolge nach Steuercode sortiert ist.

## <a name="example-4-queryable-data-sources"></a><a name="example-4"></a>Beispiel 4: Abfragbare Datenquellen

Wenn **TaxTransaction** als ER-Datenquelle vom Typ *Tabellendatensätze* konfiguriert ist, die sich auf die Tabelle **TaxTrans** bezieht, kann die ER-Datenquelle **TaxTransactionFiltered** so konfiguriert werden, dass sie den Ausdruck `FILTER(TaxTransaction, TaxCode="VAT19")` enthält, der Transaktionen für einen bestimmten Steuercode abruft. Da die konfigurierte **TaxTransactionFiltered** ER Datenquelle abfragbar ist, kann der Ausdruck `ORDERBY ("Query", TaxTransactionFiltered, TaxTransactionFiltered.TransDate)` so konfiguriert werden, dass er die Liste der gefilterten Steuertransaktionen zurückgibt, die nach Transaktionsdatum in aufsteigender Reihenfolge sortiert ist.

Wenn Sie **TaxTransactionOrdered** als ER-Datenquelle vom Typ *Berechnetes Feld* konfigurieren, die den Ausdruck `ORDERBY ("Query", TaxTransaction, TaxTransaction.TransDate)` enthält, und eine ER-Datenquelle vom Typ *Berechnetes Feld*, die den Ausdruck `FILTER(TaxTransactionOrdered, TaxCode="VAT19")` enthält, tritt zur Entwurfszeit im Designer für die Zuordnung von ER-Modellen ein Validierungsfehler [auf](er-components-inspections.md#i18). Dieser Fehler tritt auf, weil das erste Argument der Funktion [FILTER](er-functions-list-filter.md#usage-notes) auf eine abfragbare ER-Datenquelle verweisen muss, aber die Datenquelle **TaxTransactionOrdered**, die die Funktion `ORDERBY` enthält, ist nicht abfragbar.

## <a name="example-5-comparability"></a><a name="example-5"></a>Beispiel 5: Vergleichbarkeit

### <a name="prerequisites"></a>Voraussetzungen

1. Geben Sie eine Datenquelle **DS1** vom Typ *Berechnetes Feld* ein, die den Ausdruck `SPLIT ("D1|_D2|D3", "|")` enthält.
2. Öffnen Sie die Seite **[Finanzielle Dimensionswerte](../../../finance/general-ledger/financial-dimensions.md)**, und wählen Sie die Dimension **CostCenter**.
3. Geben Sie die folgenden Werte für die Dimensionen ein: **D1**, **\_D2**, und **D3**.

### <a name="sorting-in-memory"></a>Sortieren im Speicher

1. Konfigurieren Sie die Datenquelle **DS2** vom Typ *Berechnetes Feld*, die den Ausdruck `ORDERBY("InMemory", DS1, DS1.Value)` enthält.
2. Beachten Sie, dass der Ausdruck `FIRST(DS2).Value` den Textwert **"D1"** zurückgibt, der Ausdruck `INDEX(DS2, COUNT(DS2)).Value` den Textwert **"\_D2"** und der Ausdruck `STRINGJOIN(DS2, DS2.Value, "|")` den Textwert **"D1\|D3\|\_D2"** zurückgibt.

### <a name="sorting-in-database"></a>Sortieren in der Datenbank

1. Geben Sie die Datenquelle **DS3** vom Typ *Tabellensätze* ein, die auf die Entität **FinancialDimensionValueEntity** verweist.
2. Konfigurieren Sie die Datenquelle **DS4** des Typs *Berechnetes Feld*, die den Ausdruck `FILTER(DS3, DS3.FinancialDimension="CostCenter")` enthält.
3. Konfigurieren Sie die Datenquelle **DS5** des Typs *Berechnetes Feld*, die den Ausdruck `ORDERBY(DS4, DS4.DimensionValue)` enthält.
4. Beachten Sie, dass der Ausdruck `FIRST(DS5).Value` den Textwert **"\_D2"**, der Ausdruck `INDEX(DS5, COUNT(DS5)).Value` den Textwert **"D3"** und der Ausdruck `STRINGJOIN(DS5, DS5.Value, "|")` den Textwert **"\_D2\|D1\|D3"** zurückgibt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
