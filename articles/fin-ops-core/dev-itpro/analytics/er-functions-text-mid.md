---
title: MID EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der MID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 1d8a7d2e9beb0fc8724d26de0acaf1d61e3834c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680289"
---
# <a name="mid-er-function"></a>MID EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `MID` gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab der angegebenen Zeichenfolge angibt, wobei an der angegebenen Position gestartet wird.

## <a name="syntax"></a>Syntax

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Wert *String*, der den Text angibt, von dem Zeichen zurückgegeben werden sollen.

`starting position`: *Integer*

Der Wert *Integer*, der die Position des ersten Zeichens angibt, das aus dem angegebenen Text zurückgegeben werden muss.

`number of characters`: *Integer*

Der Wert *Integer*, der die Anzahl der Zeichen angibt, die von der angegebenen Startposition aus zurückgegeben werden müssen.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn der Wert des Arguments `starting position` weniger als 0 (null) beträgt, werden die Zeichen, die zurückgegeben werden, ab der ersten Position in der angegebenen Zeichenfolge zurückgegeben.

Wenn der Wert des Arguments `starting position` die Länge der angegebenen Zeichenfolge überschreitet, wird eine leere Zeichenfolge zurückgegeben.

## <a name="example"></a>Beispiel

`MID ("Sample", 2, 3)` gibt **"amp"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
