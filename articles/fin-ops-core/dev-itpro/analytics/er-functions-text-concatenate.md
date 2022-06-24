---
title: CONCATENATE EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der CONCATENATE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 926c3acf92fc8017c3c4a7814855a6871c1cacc4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8863263"
---
# <a name="concatenate-er-function"></a>CONCATENATE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `CONCATENATE` gibt alle angegebenen Textzeichenfolgen mit dem Wert *String* zurück, nachdem sie zu einer Zeichenfolge zusammengefügt wurden.

## <a name="syntax"></a>Syntax

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a>Argumente

`text 1`: *String*

Ein Verweis auf eine Datenquelle des Datensatztyps *String*. Dieses Argument ist erforderlich.

`text N`: *String*

Ein Verweis auf eine Datenquelle des Datensatztyps *String*. Diese zusätzlichen Argumente sind optional.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`CONCATENATE ("abc", "def")` gibt **"abcdef"** zurück.

## <a name="usage-notes"></a>Anwendungshinweise

Der Ausdruck `"abc" & "def"` gibt auch **"abcdef"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]