---
title: NULLDATETIME EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung von NULLDATETIME bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: kfend
ms.date: 12/04/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 49b75a6cc1e2c1eee926ed8a235ae886d781ad3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287277"
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
