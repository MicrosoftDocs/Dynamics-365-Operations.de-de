---
title: INTVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von INTVALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 98b91a983c60bb99280763f7f7a944d08f535e60
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686002"
---
# <a name="intvalue-er-function"></a>INTVALUE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `INTVALUE` gibt den Wert *Int* zurück, der die angegebene Zeichenfolge darstellt.

## <a name="syntax-1"></a>Syntax 1

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a>Syntax 2

```vb
INTVALUE (number)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Ein Textwert, der in die Zahl *Int* konvertiert werden muss.

`number`: *Real* oder *Integer*

Der numerische Wert *Real* oder *Integer*, der in die Zahl *Int* konvertiert werden muss.

## <a name="return-values"></a>Rückgabewerte

*Int*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Sämtliche Dezimalstellen werden abgeschnitten.

## <a name="example-1"></a>Beispiel 1

`INTVALUE ("100.77")` gibt den *Int*-Wert **100** zurück.

## <a name="example-2"></a>Beispiel 2

`INTVALUE (-100.77)` gibt den *Int*-Wert **-100** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Funktionen zur Typenumrechnung](er-functions-category-type-conversion.md)
