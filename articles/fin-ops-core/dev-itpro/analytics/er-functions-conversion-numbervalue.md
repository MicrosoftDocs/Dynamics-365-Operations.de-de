---
title: NUMBERVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von NUMBERVALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/05/2019
ms.topic: article
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755347"
---
# <a name="numbervalue-er-function"></a>NUMBERVALUE EB-Funktion

[!include [banner](../includes/banner.md)]

Diese Funktion `NUMBERVALUE` gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird. Bei der Konvertierung werden die angegebenen Trennzeichen für Dezimal- und Zifferngruppierungen berücksichtigt.

## <a name="syntax"></a>Syntax

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Ein Textwert, der in die Zahl *Real* konvertiert werden muss.

`decimal separator`: String

Ein Dezimaltrennzeichen. Es wird verwendet, um die ganze Zahl und die Bruchteile einer Dezimalzahl zu trennen.

`digit grouping separator`: *String*

Ein Trennzeichen für Zifferngruppen. Es wird als Tausendertrennzeichen verwendet.

## <a name="return-values"></a>Rückgabewerte

*Gleitkommazahl*

Der resultierende numerische Wert.

## <a name="example"></a>Beispiel

`NUMBERVALUE( "1 234,56", ",", " ")` gibt **1234.56** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Funktionen zur Typenumrechnung](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]