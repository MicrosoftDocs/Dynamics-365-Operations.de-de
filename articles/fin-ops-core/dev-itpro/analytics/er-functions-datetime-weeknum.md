---
title: WEEKNUM EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der WEEKNUM-Funktion bei der elektronischen Berichterstellung bereitgestellt.
author: kfend
ms.date: 01/15/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.custom: 58771
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 4658f88b7e353e651177fad0c8636c5403be1256
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268145"
---
# <a name="weeknum-er-function"></a>WEEKNUM EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `WEEKNUM` gibt einen *[Ganzzahl](er-formula-supported-data-types-primitive.md#integer)*-Wert zurück, der die Wochen im Jahr mit einem bestimmten *[Date](er-formula-supported-data-types-primitive.md#date)*-Wert darstellt. Die Berechnung basiert auf kulturabhängigen Regeln, die eine Kalenderwoche und den ersten Tag der Woche definieren.

## <a name="syntax"></a>Syntax

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumente</a>

`date`: *Date*

Ein Datumswert, der das für die Berechnung der Woche des Jahres zu verwendende Datum darstellt.

`culture`: *[Zeichenfolge](er-formula-supported-data-types-primitive.md#string)*

Die zum Berechnen zu verwendende Kultur. Sie können Kulturcodes verwenden, die gemäß .NET-[Standards](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0) unterstützt werden.

## <a name="return-values"></a>Rückgabewerte

*Ganzzahl*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Die Woche des Jahres wird auf der Grundlage des [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)-Standards berechnet, wenn dieser Standard von einem Land oder einer Region übernommen wurde, für das das Gebietsschema zur Laufzeit bereitgestellt wird. Ansonsten basiert die Berechnung auf länder-/regionsspezifischen nationalen Standards.

Wenn ein nicht unterstützter [Kultur](#arguments)code als Argument der `WEEKNUM`-Funktion zur Laufzeit bereitgestellt wird, wird eine Ausnahme ausgelöst. Wenn die leere Zeichenfolge als Kulturcode bereitgestellt wird, wird der englische länderneutrale Kalender verwendet, um die Wochennummer zu berechnen.

## <a name="examples"></a>Beispiele

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` gibt **1** zurück.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` gibt **53** zurück.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` gibt **52** zurück.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` gibt **21** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
