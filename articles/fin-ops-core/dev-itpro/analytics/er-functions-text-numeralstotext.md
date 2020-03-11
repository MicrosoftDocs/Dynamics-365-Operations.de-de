---
title: NUMERALSTOTEXT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NUMERALSTOTEXT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 31fd4076d04ce7d849555bc8301c4d23ad8e1a7e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041008"
---
# <a name="NUMERALSTOTEXT">NUMERALSTOTEXT EB-Funktion</a>

[!include [banner](../includes/banner.md)]

Die Funktion `NUMERALSTOTEXT` gibt die angegebene Zahl mit dem Wert *String* zurück, nachdem er in der angegebenen Sprache geschrieben (d. h. in Textzeichenfolgen konvertiert) wurde.

## <a name="syntax"></a>Syntax

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumente

`number`: *Integer* oder *Real*

Ein numerischer Wert, der die Nummer angibt, die ausgeschrieben werden muss.

`language`: *String*

Der Wert *String*, der den Sprachcode darstellt.

`currency`: *String*

Der Wert *String*, der den Währungscode darstellt.

`print currency name flag`: *Boolesch*

Ein *boolescher* Wert, der angibt, ob dem ausgeschriebenen Text ein Währungsname hinzugefügt werden muss.

`decimal points`: *Integer*

Der Wert *Integer*, der die Anzahl der Dezimalstellen angibt, die der ausgeschriebene Text haben sollte.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Der Sprachcode ist optional. Wenn er als leere Zeichenfolge definiert ist, wird stattdessen der Sprachcode für den ausgeführten Kontext verwendet. Der Standard-Sprachcode lautet **EN-US**. Der Sprachcode für den laufenden Kontext ist im Element **Ordner** oder **Datei** des Formats der elektronischen Berichterstellung (EB) definiert, das ausgeführt wird.

Der Währungscode ist optional. Wenn er als leere Zeichenfolge definiert ist, wird stattdessen die Unternehmenswährung für den ausgeführten Kontext verwendet.

> [!NOTE] 
> Die Argumente `print currency name flag` und `decimal points` werden nur für die folgenden Sprachcodes analysiert: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** und **RU**. Darüber hinaus wird das Argument `print currency name flag` nur für Unternehmen analysiert, bei denen der Landes- oder Regionskontext die Deklination von Währungsnamen unterstützt.

## <a name="example-1"></a>Beispiel 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` gibt **"One Thousand Two Hundred Thirty Four and 56"** zurück.

## <a name="example-2"></a>Beispiel 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` gibt **"Sto dwadzieścia"** zurück. 

## <a name="example-3"></a>Beispiel 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` gibt **"Сто двадцать евро 21 евроцент"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)
