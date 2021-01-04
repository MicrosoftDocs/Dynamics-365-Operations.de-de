---
title: UPPER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der UPPER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: c3e594138ef8e28f1b3aaf333026fa8f9e55cca0
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688340"
---
# <a name="upper-er-function"></a>UPPER EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `UPPER` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Großbuchstaben umgewandelt wurde.

## <a name="syntax"></a>Syntax

```vb
UPPER (text )
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der gültige Pfad einer Datenquelle des Typs *String*.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`UPPER ("Sample")` gibt **"SAMPLE"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
