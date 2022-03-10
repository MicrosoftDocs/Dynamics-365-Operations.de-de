---
title: JSONVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der JSONVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 10/25/2021
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
ms.openlocfilehash: ff33098e5be4dd9748d01d45b596360617305724
ms.sourcegitcommit: f8b597b09157d934b62bd5fb9a4d05b8f82b5a0e
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/26/2021
ms.locfileid: "7700062"
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

Der Bezeichner eines Skalarwerts der JSON-Daten. Verwenden Sie einen Schrägstrich (/), um die Namen verwandter JSON-Knoten zu trennen. Verwenden Sie die Notation mit eckigen Klammern  (\[\]) , um den Index eines bestimmten Werts in einem JSON-Array anzugeben. Beachten Sie, dass für diesen Index eine nullbasierte Nummerierung verwendet wird.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example-1"></a>Beispiel 1

Die Datenquelle **JsonField** enthält die folgenden Daten im JSON-Format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. In diesem Fall gibt der Ausdruck `JSONVALUE (JsonField, "BuildNumber")` den folgenden Wert des Datentyps *String* zurück: **"7.3.1234.1"**.

## <a name="example-2"></a>Beispiel 2

Die Datenquelle **JsonField** des Typs *Berechnetes Feld* enthält den folgenden Ausdruck: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Dieser Ausdruck ist so konfiguriert, dass er einen [*Zeichenfolge*](er-formula-supported-data-types-primitive.md#string)-Wert zurückgibt, der die folgenden Daten im JSON-Format darstellt.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

In diesem Fall gibt der Ausdruck `JSONVALUE(json, "workers/[1]/emails/[0]")` den folgenden Wert des *Zeichenfolge*-Datentyps zurück: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
