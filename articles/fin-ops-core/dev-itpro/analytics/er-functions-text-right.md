---
title: RIGHT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der RIGHT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd53ece77b08fc9723c838da5ba08bf3825b5e56
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743710"
---
# <a name="right-er-function"></a>RIGHT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `RIGHT` gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab dem Ende der angegebenen Zeichenfolge angibt.

## <a name="syntax"></a>Syntax

```vb
RIGHT (text, number)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Wert *String*, der den Originaltext darstellt.

`number`: *Integer*

Die Anzahl der Zeichen, die vom Ende des Originaltexts zurückgegeben werden müssen.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`RIGHT ("Sample", 3)` gibt **"ple"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
