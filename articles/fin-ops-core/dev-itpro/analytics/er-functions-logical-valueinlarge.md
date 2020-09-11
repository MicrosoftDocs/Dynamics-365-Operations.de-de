---
title: VALUEINLARGE-EB-Funktion
description: Dieses Thema bietet Informationen zur Verwendung der VALUEINLARGE-Funktion der elektronischen Berichterstellung (EB).
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705142"
---
# <a name="valueinlarge-er-function"></a>VALUEINLARGE-EB-Funktion

[!include [banner](../includes/banner.md)]

Die `VALUEINLARGE`-Funktion bestimmt, ob die angegebene Eingabe des Typs *Int64* oder *Integer* mit irgendeinem Wert eines angegebenen Artikels in der angegebenen Liste übereinstimmt. Die Funktion gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Eingabe mit dem Ergebnis der Ausführung des angegebenen Ausdrucks für mindestens einen Datensatz der entsprechenden Liste übereinstimmt. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück. Um den Unterschied zur `VALUEIN`-Funktion zu verstehen, sehen Sie den Abschnitt [Verwendungshinweis](#usage_note) später in diesem Thema.

## <a name="syntax"></a>Syntax

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumente

`input`: *Feld*

Der gültige Pfad eines Datenquellenelements des Typs *Datensatzliste*. Der Wert dieses Elements, der abgeglichen wird.

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`list item expression`: *Ausdruck*

Ein gültiger Bedingungsausdruck , der entweder zu einem Feld zeigt oder ein einzelnes Feld der Liste enthält, die zum Abgleich verwendet werden soll.

## <a name="return-values"></a>Rückgabewerte

*Aktiv*

Der resultierende *boolesche* Wert.

## <a name=""></a><a name="usage_note">Anwendungshinweise</a>

Wenn die angegebene Eingabe einen Typ *Int64* oder *Integer* eines Datenquellenelements darstellt, deren Aufruf in eine direkte SQL-Anweisung übersetzt werden kann, wird die angegebene Liste in eine temporäre SQL-Tabelle konvertiert und der Abgleich erfolgt in der Datenbank, indem eine einzelne `EXISTS JOIN`-Abfrage ausgeführt wird. Andernfalls funktioniert diese Funktion als [`VALUEIN`](er-functions-logical-valuein.md)-Funktion.

Wenn die angegebene Eingabe ein Datenquellenelement darstellt, das als ein anderes Element als der Typ *Int64* und *Integer* konzipiert ist, tritt zur Entwurfszeit ein Fehler auf, der Sie darüber informiert, dass die `VALUEINLARGE`-Funktion für den konfigurierten EB-Ausdruck nicht anwendbar ist.

Wenn der `VALUEINLARGE`-Funktionsausdruck ausgeführt wird und mehr als eine temporäre Tabelle im Rahmen dieser Ausführung verwendet, tritt ein Laufzeitfehler auf.

## <a name="example"></a>Beispiel

Die folgenden Datenquellen definieren Sie in Ihrer Modellzuordnung:

- Die Datenquelle **In** des Typs *Tabellendatensätze*.
    - Diese Datenquelle bezieht sich auf die **Intrastat**-Tabelle.
    - Die Option **Unternehmensübergreifend** ist auf **Nein** festgelegt.
- Die Datenquelle **InMemory** des Typs *Berechnetes Feld*.
    - Diese Datenquelle enthält den Ausdruck `WHERE (In, In.Port <> "")`.
- Die Datenquelle **InFiltered** des Typs *Berechnetes Feld*.
    - Diese Datenquelle enthält den Ausdruck `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Wenn die Datenquelle **InFiltered** im Rahmen des Unternehmens **DEMF** aufgerufen wird, wird eine neue temporäre Tabelle in der Anwendungsdatenbank erstellt, die gesammelte In-Memory-Liste von Datensatzkennungscodes werden in diese Tabelle eingefügt und die folgende SQL-Anweisung wird generiert, um gefilterte Datensätze der **Intrastat**-Tabelle zurückzugeben.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Logische Funktionen](er-functions-category-logical.md)

[VALUEIN-Funktionen](er-functions-logical-valuein.md)
