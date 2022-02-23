---
title: DAYOFYEAR EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der DAYOFYEAR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: b9b937e7fae3e90d1a87196fab653dfac8e94179
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682388"
---
# <a name="dayofyear-er-function"></a>DAYOFYEAR EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `DAYOFYEAR` gibt einen Wert für *Integer* zurück, der die Anzahl der Tage zwischen dem 01. Januar und dem angegebenen Datum darstellt.

## <a name="syntax"></a>Syntax

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a>Argumente

`date`: *Date*

Ein Datumswert, der das für die Berechnung der Anzahl der Tage zu verwendende Datum darstellt.

## <a name="return-values"></a>Rückgabewerte

*Ganze Zahl*

Der resultierende numerische Wert.

## <a name="example-1"></a>Beispiel 1

`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` gibt **61** zurück.

## <a name="example-2"></a>Beispiel 2

`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` gibt **1** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)
