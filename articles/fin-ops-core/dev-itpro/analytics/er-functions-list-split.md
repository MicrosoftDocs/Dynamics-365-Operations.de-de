---
title: SPLIT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SPLIT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 4a42b0c7cfa2a8d3dcb7448224c9e88a48276f7d8cdbcce484383a778b8275a5
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6757320"
---
# <a name="split-er-function"></a>SPLIT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `SPLIT` teilt die angegebene Eingabezeichenfolge in Teilzeichenfolgen auf und gibt das Ergebnis als neuen Wert *Datensatzliste* zurück.

## <a name="syntax-1"></a>Syntax 1

```vb
SPLIT (input, length)
```

Diese Syntax wird verwendet, um die angegebene Eingabezeichenfolge in Teilzeichenfolgen aufzuteilen, von denen jede die angegebene Länge hat.

## <a name="syntax-2"></a>Syntax 2

```vb
SPLIT (input, delimiter)
```

Diese Syntax wird verwendet, um die angegebene Eingabezeichenfolge in Teilzeichenfolgen zu teilen, von denen jede die angegebene Länge hat.

## <a name="arguments"></a>Argumente

`input`: *String*

Zu trennender Text.

`length`: *Integer*

Die maximale Länge einer einzelnen Teilzeichenfolge.

`delimiter`: *String*

Ein Trennzeichen, das zum Trennen von Teilzeichenfolgen verwendet wird.

## <a name="return-values"></a>Rückgabewerte

*Datensatzliste*

Die resultierende Liste der Datensätze.

## <a name="usage-notes"></a>Anwendungshinweise

Die Datensatzstruktur der zurückgegebenen Liste besteht aus dem Feld **Wert** des Typs *String*. Jeder Datensatz der zurückgegebenen Liste enthält generierte Teilzeichenfolgen in diesem Feld.

Wenn das Argument `delimiter` leer ist, besteht die neue Liste, die zurückgegeben wir, aus einem Datensatz, der das Feld **Wert** des Typs *String* enthält. Dieses Feld enthält den Eingabetext.

Falls das Argument `input` leer ist, wird eine neue leere Liste zurückgegeben. Wenn entweder das Argument `input` oder `delimiter` nicht definiert (null) ist, wird eine Anwendungsausnahme ausgelöst.

## <a name="example-1"></a>Beispiel 1

`SPLIT ("abcd", 3)` gibt eine neue Liste zurück, die aus zwei Datensätzen besteht, die das Feld **Wert** des Typs *String* aufweisen. Das Feld **Wert** im ersten Datensatz enthält den Text **"abc"**, und das Feld **Wert** im zweiten Datensatz enthält den Text **"d"**.

## <a name="example-2"></a>Beispiel 2

`SPLIT ("XAb aBy", "aB")` gibt eine neue Liste zurück, die aus drei Datensätzen besteht, die das Feld **Wert** des Typs *String* aufweisen. Das Feld **Wert** im ersten Datensatz enthält den Text **"X"**, das Feld **Wert** im zweiten Datensatz enthält den Text **"&nbsp;"**, und das Feld **Wert** im dritten Datensatz enthält den Text **"y"**. 

## <a name="example-3"></a>Beispiel 3

Sie können die Funktion [INDEX](er-functions-list-index.md) zum Zugriff auf einzelne Elemente der angegebenen Eingabezeichenfolge verwenden. Wenn Sie die Datenquelle **MyList** des Typs **Berechnetes Feld** eingeben, und auf den Ausdruck `SPLIT("abc", 1)` konfigurieren, gibt der Ausdruck `INDEX(MyList,2).Value` den Text **„A“** zurück.

## <a name="example-4"></a>Beispiel 4

Die Funktion [AUFZÄHLEN](er-functions-list-enumerate.md) auch zum Zugriff auf einzelne Elemente der angegebenen Eingabezeichenfolge verwenden. Wenn Sie zuerst die Datenquelle **MyList** des Typs **Berechnetes Feld** eingeben und sie auf den Ausdruck `SPLIT("abc", 1)` konfigurieren und dann die Datenquelle **EnumeratedList** des Typs **Berechnetes Feld** eingeben und dafür den Ausdruck `ENUMERATE(MyList)` konfigurieren, gibt der Ausdruck `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` den Text **„B“** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
