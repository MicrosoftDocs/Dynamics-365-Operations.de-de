---
title: TRANSLATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von TRANSLATE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: c5d192b8679d6df2c44a0038fe4ffc181a6a54df
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685302"
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