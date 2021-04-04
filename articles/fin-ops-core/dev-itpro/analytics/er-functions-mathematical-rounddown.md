---
title: ROUNDDOWN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUNDDOWN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: f199d662eb31f184b6f978b3d251e64907254584
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567139"
---
# <a name="rounddown-er-function"></a>ROUNDDOWN EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ROUNDDOWN` gibt die angegebene Zahl mit dem Wert *Real* zurück, nachdem sie auf die angegebene Zahl der Dezimalstellen abgerundet wurde.

## <a name="syntax"></a>Syntax

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a>Argumente

`number`: *Real*

Ein numerischer Wert, der abgerundet werden muss.

`decimals`: *Integer*

Ein numerischer Wert, der die Anzahl der Dezimalstellen angibt.

## <a name="return-values"></a>Rückgabewerte

*Gleitkommazahl*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Diese Funktion verhält sich wie [RUNDUNG](er-functions-mathematical-round.md), rundet die angegebene Zahl aber immer ab (in Richtung null).

## <a name="example-1"></a>Beispiel 1

`ROUNDDOWN (1200.767, 2)` rundet auf bis zu zwei Dezimalstellen ab und gibt den Wert **1200.76** zurück. 

## <a name="example-2"></a>Beispiel 2

`ROUNDDOWN (1700.767, -3)` rundet auf das nächste Vielfache von 1.000 ab und gibt den Wert **1000** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Rechenoperationen](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]