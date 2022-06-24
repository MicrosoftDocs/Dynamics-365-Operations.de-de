---
title: NULLDATETIME EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung von NULLDATETIME bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: 3e8447d4f05ee8394842b9b07d14d1c054834bb2
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867671"
---
# <a name="nulldatetime-er-function"></a>NULLDATETIME EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `NULLDATETIME` gibt den Wert *DateTime* zurück, der den Wert für Datum/Uhrzeit **null** (01. Januar 1900) in Koordinierter Weltzeit (Greenwich Mean Time \[GMT\]) darstellt.

## <a name="syntax"></a>Syntax

```vb
NULLDATETIME ()
```

## <a name="return-values"></a>Rückgabewerte

*DateTime*

Der resultierende Wert für Datum/Uhrzeit.

## <a name="example"></a>Beispiel

`DATETIMEFORMAT( NULLDATETIME(), "O")` gibt den Zeichenkettenwert **1900-01-01T00:00:00.0000000+00:00** zurück, wenn er während eines Prozesses aufgerufen wird, der von einem Anwendungsbenutzer mit dem Zeitzonenwert **(GMT Koordinierte Weltzeit)** im Bereich **Sprach- und Länder-/Regionsvoreinstellungen** initiiert wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]