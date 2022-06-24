---
title: NUMBERFORMAT EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der NUMBERFORMAT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 3e6fa4cbdfb2509418a40980aa29894b5e531bbb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8862189"
---
# <a name="numberformat-er-function"></a>NUMBERFORMAT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `NUMBERFORMAT` gibt den Wert *String* zurück, der eine angegebene Zahl im angegebenen Format und in einer optional angegebenen [Kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt. Informationen zu unterstützten Formaten finden Sie unter [Standard](/dotnet/standard/base-types/standard-numeric-format-strings) und [Benutzerdefiniert](/dotnet/standard/base-types/custom-numeric-format-strings).

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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]