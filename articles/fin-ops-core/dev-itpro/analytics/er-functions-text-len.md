---
title: LEN EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der LEN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 12/11/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 5a8e672e0308a58dca28c73ce01c7307abec60ed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280124"
---
# <a name="len-er-function"></a>LEN EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `LEN` gibt die angegebene Anzahl von Zeichen in der angegebenen Zeichenfolge mit dem Wert *Integer* zurück.

## <a name="syntax"></a>Syntax

```vb
LEN (text)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Wert *String*, der den Text angibt.

## <a name="return-values"></a>Rückgabewerte

*Ganze Zahl*

Der resultierende numerische Wert.

## <a name="example"></a>Beispiel

`LEN ("Sample")` gibt **6** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
