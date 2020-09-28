---
title: LOWER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LOWER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 12577e571c8e87db79395895e2a22e66ee7df32c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745680"
---
# <a name="lower-er-function"></a>LOWER EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `LOWER` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Kleinbuchstaben umgewandelt wurde.

## <a name="syntax"></a>Syntax

```vb
LOWER (text)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Wert *String*, der den Text angibt.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`LOWER ("Sample")` gibt **"sample"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
