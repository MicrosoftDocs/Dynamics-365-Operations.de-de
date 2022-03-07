---
title: WEEKNUM EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der WEEKNUM-Funktion bei der elektronischen Berichterstellung bereitgestellt.
author: NickSelin
ms.date: 12/03/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: fe36d4142b6e4922e2cbca09bb0ca9f68f6680a0
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891342"
---
# <a name="weeknum-er-function"></a>WEEKNUM EB-Funktion

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

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
