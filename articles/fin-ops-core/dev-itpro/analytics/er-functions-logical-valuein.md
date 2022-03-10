---
title: VALUEIN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der VALUEIN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/14/2021
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
ms.openlocfilehash: efa811df360b2ca38eb59bac849e70041405fa81
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922361"
---
# <a name="valuein-er-function"></a>VALUEIN EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `VALUEIN` bestimmt, ob die Eingabe mit einem angegebenen Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt. Sie gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.

## <a name="syntax"></a>Syntax

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumente

`input`: *Feld*

Der gültige Pfad des Elementes einer Datenquelle des Typs *Datensatzliste*. Der Wert dieses Elements, der abgeglichen wird.

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`list item expression`: *Boolesch*

Ein gültiger Bedingungsausdruck , der entweder zu einem Feld zeigt oder ein einzelnes Feld der Liste enthält, die zum Abgleich verwendet werden soll.

## <a name="return-values"></a>Rückgabewerte

*Aktiv*

Der resultierende *boolesche* Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Im Allgemeinen wird die Funktion `VALUEIN` zu einem Satz **OR**-Bedingungen umgerechnet. Wenn die Liste von **ODER**-Bedingungen groß ist und die maximale Gesamtlänge einer SQL-Anweisung überschritten werden kann, erwägen Sie die Verwendung der [`VALUEINLARGE`](er-functions-logical-valueinlarge.md)-Funktion.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

In einigen Fällen kann es in eine SQL-Datenbankanweisung durch Verwendung des Operators `EXISTS JOIN` übersetzt werden.

> [!NOTE]
> Der Wert, den die Funktion `VALUEIN` zurückgibt, wird [unterschiedlich](er-functions-list-filter.md#usage-notes) verwendet, je nachdem, ob diese Funktion zur Angabe der Auswahlkriterien für die Funktion [`FILTER`](er-functions-list-filter.md) oder die Funktion [`WHERE`](er-functions-list-where.md) verwendet wird.

## <a name="example-1"></a>Beispiel 1

In Ihrer Modellzuweisung definieren Sie die Datenquelle **Liste** des Typs *Berechnetes Feld*. Diese Datenquelle enthält den Ausdruck `SPLIT ("a,b,c", ",")`.

Beim Aufruf einer Datenquelle, wenn diese als `VALUEIN ("B", List, List.Value)`-Ausdruck konfiguriert wurde, wird **TRUE** zurückgegeben. In diesem Fall wird die Funktion `VALUEIN` in den folgenden Satz an Bedingungen umgerechnet: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, wobei `("B" = "b")` **TRUE** entspricht.

Beim Aufruf einer Datenquelle, wenn diese als `VALUEIN ("B", List, LEFT(List.Value, 0))`-Ausdruck konfiguriert wurde, wird **FALSE** zurückgegeben. In diesem Fall wird die Funktion `VALUEIN` in die folgende Bedingung umgerechnet: `("B" = "")`, was nicht **TRUE** entspricht.

Der obere Grenzwert für die Anzahl der Zeichen im Text einer derartigen Bedingung entspricht 32.768 Zeichen. Daher sollten Sie keine Datenquellen erstellen, die möglicherweise zur Laufzeit diesen Grenzwert überschreiten. Wenn das Limit überschritten wird, wird die Anwendung nicht mehr ausgeführt und eine Ausnahme ausgelöst. Beispielsweise kann diese Situation erfolgen, wenn die Datenquelle als `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)` konfiguriert wird, und die Listen **List1** und **List2** eine große Anzahl von Datensätzen enthalten.

In einigen Fällen wird die Funktion `VALUEIN` in eine Datenbankaussage durch Verwendung des Operators `EXISTS JOIN` umgerechnet. Dieses Verhalten tritt auf, wenn die Funktion [`FILTER`](er-functions-list-filter.md) verwendet wird und die folgenden Bedingungen erfüllt sind:

- Die Option **BITTEN SIE UM ABFRAGE** wird für die Datenquelle der Funktion `VALUEIN` deaktiviert, die die Liste von Datenträgen bezieht. Es werden keine zusätzliche Bedingungen auf diese Datenquelle zur Bearbeitungszeit angewendet.
- Es werden keine eingebetteten Ausdrücke für die Datenquelle der Funktion `VALUEIN` konfiguriert, die sich auf die Liste von Datenträgen bezieht.
- Ein Listenelement der Funktion `VALUEIN` bezieht sich auf ein Feld der angegebenen Datenquelle, nicht auf einen Ausdruck oder eine Methode dieser Datenquelle.

Erwägen Sie die Nutzung dieser Option anstelle der Funktion [`WHERE`](er-functions-list-where.md), die weiter oben in diesem Beispiel beschrieben wird.

## <a name="example-2"></a>Beispiel 2

Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:

- Die Datenquelle **In** des Typs *Tabellendatensätze*. Diese Datenquelle bezieht sich auf die Intrastat-Tabelle.
- Die Datenquelle **Port** des Typs *Tabellendatensätze*. Diese Datenquelle bezieht sich auf die IntrastatPort-Tabelle.

Wenn eine Datenquelle angerufen wird, die als Ausdruck `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` konfiguriert, wird die nächste SQL-Anweisung generiert, um gefilterte Datensätze der Intrastat-Tabelle zurückzugeben.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

Für **dataAreaId**-Felder wird die endgültige SQL-Anweisung durch die Verwendung des Operators `IN` generiert.

## <a name="example-3"></a>Beispiel 3

Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:

- Die Datenquelle **Le** des Typs *Berechnetes Feld*. Diese Datenquelle enthält den Ausdruck `SPLIT ("DEMF,GBSI,USMF", ",")`.
- Die Datenquelle **In** des Typs *Tabellendatensätze*. Diese Datenquelle bezieht sich auf die Intrastat-Tabelle und die Option **Unternehmensübergreifend** ist dafür aktiviert.

Wenn eine Datenquelle angerufen wird, die als Ausdruck `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` konfiguriert wird, enthält die abschließende SQL-Anweisung die folgende Bedingung.

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Logische Funktionen](er-functions-category-logical.md)

[VALUEINLARGE-Funktionen](er-functions-logical-valueinlarge.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
