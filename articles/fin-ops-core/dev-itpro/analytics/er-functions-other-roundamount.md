---
title: ROUNDAMOUNT EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der ROUNDAMOUNT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 623024f4ee6ac0d237ec45d50d9678195d6c6cd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905169"
---
# <a name="roundamount-er-function"></a>ROUNDAMOUNT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ROUNDAMOUNT` gibt den Wert *Real* zurück, der das Ergebnis der Rundung des angegebenen Betrags auf das nächste Vielfache der angegebenen Anzahl gemäß der angegebenen Rundungsregel darstellt.

## <a name="syntax"></a>Syntax

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a>Argumente

`number`: *Int* oder *Real*

Ein numerischer Wert, der gerundet werden muss.

`decimals`: *Int* oder *Real*

Die Zahl, die der Wert des Parameters `number` auf ein Vielfaches gerundet werden muss.

`round rule`: *Enum value*

Ein Aufzählungswert der Aufzählung **RoundOffType**, die die Rundungsregel definiert. Diese Aufzählung bietet die folgenden Werte:

- Normal (gewöhnlich)
- Abrunden (RoundDown)
- Aufrunden (RoundUp)

## <a name="return-values"></a>Rückgabewerte

*Gleitkommazahl*

Der sich ergebende numerische Wert ist ein Vielfaches des Wertes, der durch den Parameter `decimals` angegeben wird, und kommt dem durch den Parameter `number` angegebenen Wert am nächsten.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn der Parameter `number` Null ist, gibt diese Funktion immer Null zurück.

Wenn der Parameter `decimals` Null ist, rundet diese Funktion auf den Standardrundungswert. Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, beträgt der Standardrundungswert **0,01**. Andernfalls beträgt der Standardrundungswert **1,0**.

Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, rundet diese Funktion auf den nächsten Rundungsbetrag.

Wenn der Parameter `round rule` auf **RoundOffType.RoundDown** festgelegt ist, rundet diese Funktion in Richtung Null auf den nächsten Rundungsbetrag.

Wenn der Parameter `round rule` auf **RoundOffType.RoundUp** festgelegt ist, rundet diese Funktion weg von Null auf den nächsten Rundungsbetrag.

Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, verhält sich diese Funktion wie die [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-Funktion und die [ROUND](../dev-ref/xpp-math-run-time-functions.md#round) X++ Funktion.

## <a name="remarks"></a>Bemerkungen

Um einen numerischen Wert auf eine bestimmte Anzahl von Dezimalstellen zu runden, verwenden Sie die Funktion [ROUND](er-functions-mathematical-round.md).

## <a name="example"></a>Beispiel

Wenn der Parameter **model.RoundOff** auf **RoundOffType.Ordinary** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 zurück. 

Wenn der Parameter **model.RoundOff** auf **RoundOffType.RoundDown** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 zurück. 

Wenn der Parameter **model.RoundOff** auf **RoundOffType.RoundUp** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4 zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)

[Rechenoperationen](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]