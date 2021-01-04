---
title: PADLEFT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der PADLEFT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 268941d8bc0bd4dc6de6d2597c05a11c1f530f15
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680145"
---
# <a name="padleft-er-function"></a>PADLEFT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `PADLEFT` gibt den Wert *String* mit der angegebenen Länge zurück, bei der der Anfang der angegebenen Zeichenfolge mit den angegebenen Zeichen aufgefüllt ist.

## <a name="syntax"></a>Syntax

```vb
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Wert *String*, der den Originaltext darstellt.

`length`: *Integer*

Der Wert *Integer*, der die endgültige Anzahl von Zeichen in der aufgefüllten Zeichenfolge darstellt.

`padding chars`: *String*

Die Zeichen, die zum Auffüllen verwendet werden sollen.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`PADLEFT ("1234", 10, "`&nbsp;`")` gibt die Textzeichenfolge **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
