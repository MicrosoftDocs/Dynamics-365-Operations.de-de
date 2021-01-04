---
title: NUMBERFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NUMBERFORMAT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 2c3907d1d2c74c852f4f90731e5f4bc23bfbd717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680265"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `NUMBERFORMAT` gibt den Wert *String* zurück, der eine angegebene Zahl im angegebenen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt. Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntax 1

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a>Syntax 2

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a>Argumente

`number`: *Integer* oder *Real*

Ein numerischer Wert, der die Nummer angibt, die formatiert werden muss.

`format`: *String*

Der Wert *String*, der das Format darstellt.

`culture`: *String*

Der Wert *String*, der die für die Formatierung zu verwendende Kultur darstellt.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, bestimmt der Kontext, in dem diese Funktion ausgeführt wird, die Kultur, die zum Formatieren von Zahlen verwendet wird.

## <a name="example-1"></a>Beispiel 1

Für die Kultur **EN-US** gibt `NUMBERFORMAT (0.45, "p")` **"45.00 %"** und `NUMBERFORMAT (10.45, "#")` **"10"** zurück.

## <a name="example-2"></a>Beispiel 2

`NUMBERFORMAT (10/3, "F2", "de")` gibt **3,33** zurück, wobei `NUMBERFORMAT (10/3, "F2", "en-us")` **3.33** zurückgibt.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
