---
title: JSONVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der JSONVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: b034755602a2f999892d2b976c80550b7a3d7f3cd179816dd7aa1edefe6a0270
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733772"
---
# <a name="jsonvalue-er-function"></a>JSONVALUE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `JSONVALUE` analysiert Daten im JavaScript Object Notation (JSON)-Format, auf die über den angegebenen Pfad zugegriffen wird, und sie extrahiert einen Skalarwert, der auf der angegebenen ID basiert. Anschließend wird der extrahierte Skalarwert als Wert *String* zurückgegeben.

## <a name="syntax"></a>Syntax

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumente

`input`: *String*

Der gültige Pfad einer Datenquelle des Typs *String*, die JSON-Daten enthält.

`path`: *String*

Der Bezeichner eines Skalarwerts der JSON-Daten.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

Die Datenquelle **JsonField** enthält die folgenden Daten im JSON-Format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. In diesem Fall gibt der Ausdruck `JSONVALUE (JsonField, "BuildNumber")` den folgenden Wert des Datentyps *String* zurück: **"7.3.1234.1"**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]