---
title: STRINGJOIN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der STRINGJOIN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
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
ms.openlocfilehash: 755e6481abb65dfecc8ddb6bceb032c8110095e2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568169"
---
# <a name="stringjoin-er-function"></a>STRINGJOIN EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `STRINGJOIN` gibt den Wert *String* zurück, der aus verketteten Werten des angegebenen Feldes aus der angegebenen Liste besteht. Die Werte können durch das angegebene Trennzeichen getrennt werden.

## <a name="syntax"></a>Syntax

```vb
STRINGJOIN (list, field, delimiter)
```

## <a name="arguments"></a>Argumente

`list`: *Datensatzliste*

Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.

`field`: *Feld*

Der gültige Pfad eines Feldes des Datentyps *String* in der angegebenen Liste.

`delimiter`: *String*

Ein Trennzeichen, das zum Trennen von Teilzeichenfolgen verwendet wird.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

Wenn Sie `SPLIT("abc" , 1)` als Datenquelle **DS** eingeben, gibt der Ausdruck `STRINGJOIN (DS, DS.Value, "-")` **"a-b-c"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Listenfunktionen](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]