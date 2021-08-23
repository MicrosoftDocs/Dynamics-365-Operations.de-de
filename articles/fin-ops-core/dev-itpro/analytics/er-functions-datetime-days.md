---
title: DAYS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DAYS bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 19e363e7bc8b8ad898244702ad6ba14bcf490f5ca2381b006a35dc0ed9309d49
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6750599"
---
# <a name="days-er-function"></a>DAYS EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `DAYS` gibt einen Wert für *Integer* zurück, der die Anzahl der Tage zwischen einem angegebenen Datum und einem zweiten angegebenen Datum darstellt.

## <a name="syntax"></a>Syntax

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a>Argumente

`date 1`: *Date*

Ein Datumswert, der das für die Berechnung der Anzahl der Tage zu verwendende Startdatum darstellt.

`date 2`: *Date*

Ein Datumswert, der das für die Berechnung der Anzahl der Tage zu verwendende Enddatum darstellt.

## <a name="return-values"></a>Rückgabewerte

*Ganze Zahl*

Der resultierende numerische Wert.

## <a name="usage-notes"></a>Anwendungshinweise

Die Funktion `DAYS` gibt einen positiven Wert zurück, wenn das erste Datum nach dem zweiten Datum liegt. Sie gibt **0** (null) zurück, wenn das erste Datum gleich dem zweiten Datum ist, oder sie gibt einen negativen Wert zurück, wenn das erste Datum vor dem zweiten Datum liegt.

## <a name="example"></a>Beispiel

`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` gibt **-1** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]