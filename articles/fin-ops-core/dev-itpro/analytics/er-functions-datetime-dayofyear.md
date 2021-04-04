---
title: DAYOFYEAR EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der DAYOFYEAR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: ba63c96355a6a7a1eccaddf39e47a3edb2d1e651
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563533"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]