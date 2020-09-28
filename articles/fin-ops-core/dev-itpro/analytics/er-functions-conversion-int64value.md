---
title: INT64VALUE ER Funktion
description: In diesem Thema werden Informationen zur Verwendung von INT64VALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 78b69b5280fb8c7ed99d73568097cd0c080a807a
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744838"
---
# <a name="int64value-er-function"></a>INT64VALUE ER Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `INT64VALUE` gibt den Wert *Int64* zurück, der die angegebene Zeichenfolge darstellt.

## <a name="syntax-1"></a>Syntax 1

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a>Syntax 2

```vb
INT64VALUE (number)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Ein Textwert, der in die Zahl *Int64* konvertiert werden muss.

`number`: *Real* oder *Integer*

Der numerische Wert *Real* oder *Integer*, der in die Zahl *Int64* konvertiert werden muss.

## <a name="return-values"></a>Rückgabewerte

*Int64*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Sämtliche Dezimalstellen werden abgeschnitten.

## <a name="example-1"></a>Beispiel 1

`INT64VALUE ("22565422744")` gibt den *Int64*-Wert **22565422744** zurück.

## <a name="example-2"></a>Beispiel 2

`INT64VALUE ( VALUE("22565422744.77"))` gibt den *Int64*-Wert **22565422744** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Funktionen zur Typenumrechnung](er-functions-category-type-conversion.md)
