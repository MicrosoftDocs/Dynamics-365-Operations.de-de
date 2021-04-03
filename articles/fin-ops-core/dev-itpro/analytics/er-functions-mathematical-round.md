---
title: ROUND EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUND-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 10/21/2020
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
ms.openlocfilehash: 716ac0bbc9fec992ec1bbfc99bfc86434bf97984
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570397"
---
# <a name="round-er-function"></a>ROUND EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ROUND` gibt die angegebene Zahl mit dem Wert *Real* zurück, nachdem sie auf die angegebene Zahl der Dezimalstellen gerundet wurde.

## <a name="syntax"></a>Syntax

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a>Argumente

`number`: *Real*

Ein numerischer Wert, der gerundet werden muss.

`decimals`: *Integer*

Ein numerischer Wert, der die Anzahl der Dezimalstellen angibt.

## <a name="return-values"></a>Rückgabewerte

*Gleitkommazahl*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn der Wert des Arguments `decimals` größer als 0 (null) ist, wird die angegebene Zahl auf genau so viele Dezimalstellen gerundet.

Wenn das Argument `decimals` den Wert **0** (null) hat, wird die angegebene Zahl auf die nächste gerade Ganzzahl gerundet.

Wenn der Wert des Arguments `decimals` kleiner als 0 (null) ist, wir die angegebene Zahl links der Dezimalstelle gerundet.

## <a name="example-1"></a>Beispiel 1

`ROUND (1200.767, 2)` rundet auf zwei Dezimalstellen und gibt den Wert **1200.77** zurück.

## <a name="example-2"></a>Beispiel 2

`ROUND (1200.767, -3)` rundet auf das nächste Vielfache von 1.000 und gibt den Wert **1000** zurück.

## <a name="example-3"></a>Beispiel 3

`ROUND (1200.5, 0)` rundet auf die nächste gerade Ganzahl und gibt **1200** zurück, während `ROUND (1201.5, 0)` ebenfalls eine Rundung durchführt und **1202** zurückgibt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Mathematische Funktionen](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]