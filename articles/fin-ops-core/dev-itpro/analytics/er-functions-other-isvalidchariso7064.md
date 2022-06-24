---
title: ISVALIDCHARACTERISO7064 EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der ISVALIDCHARACTERISO7064-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 43da66e79bd8fbeecf5a04283574077600552a05
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8908473"
---
# <a name="isvalidcharacteriso7064-er-function"></a>ISVALIDCHARACTERISO7064 EB-Funktion

[!include [banner](../includes/banner.md)]

Diese Funktion `ISVALIDCHARACTERISO7064` gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Zeichenfolge eine gültige internationale Bankkontonummer (IBAN) darstellt. Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.

## <a name="syntax"></a>Syntax

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Ein Textwert, der eine IBAN darstellt.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` gibt **TRUE** zurück. 

`ISVALIDCHARACTERISO7064 ("AT61")` gibt **FALSE** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]