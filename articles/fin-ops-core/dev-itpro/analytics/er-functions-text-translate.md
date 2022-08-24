---
title: TRANSLATE EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung von TRANSLATE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 04/02/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 7a15a28f6efa5333b54aa34938d22a9d6e404cec
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278440"
---
# <a name="translate-er-function"></a>TRANSLATE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `TRANSLATE` gibt einen *Zeichenfolgen* Wert zurück, der das Ergebnis der Ersetzung des angegebenen Textes in Zeichen für einen anderen bereitgestellten Zeichensatz enthält.

## <a name="syntax"></a>Syntax

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der gültige Pfad einer Datenquelle des Typs *String*.

`pattern`: *String*

Der Text, der ersetzt werden muss.

`replacement`: *String*

Den als Ersatz zu verwendenden Text.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Die `TRANSLATE` Funktion ersetzt jeweils ein Zeichen. Die Funktion ersetzt das erste Zeichen des `text` Arguments mit dem ersten Zeichen des `pattern` Arguments und dann das zweite Zeichen und folgt dem gleichen Ablauf bis zum Ende. Wenn ein Charakter aus dem `text` und `pattern` Argumente übereinstimmt, wird es durch ein Zeichen aus dem Argument `replacement` ersetzt, das sich an derselben Position befindet wie das Zeichen aus dem Argument `pattern`. Wenn ein Zeichen mehrmals im Argument `pattern` angezeigt wird, wird das Argument `replacement`, das dem ersten Auftreten dieses Zeichens entspricht, zugeordnet.

## <a name="example-1"></a>Beispiel 1

`TRANSLATE ("abcdef", "cd", "GH")` ersetzt das Zeichen **c** des angegebenen **abcdef** Texts mit dem **G** Zeichen der `replacement` Texts aus folgenden Gründen:
-   Das Zeichen **c** wird im dargestellten Text `pattern` an der ersten Stelle angezeigt.
-   Die erste Position des Texts `replacement` enthält das Zeichen **G**.

## <a name="example-2"></a>Beispiel 2

`TRANSLATE ("abcdef", "ccd", "GH")` gibt **abcdef** zurück.

## <a name="example-3"></a>Beispiel 3

`TRANSLATE ("abccba", "abc", "123")` gibt **"123321"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
