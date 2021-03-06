---
title: POWER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der POWER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: ce1f4c735f815c46003ded35156bb47febf177a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5750155"
---
# <a name="power-er-function"></a>POWER EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `POWER` gibt den Wert *Real* zurück, der das Ergebnis der Erhöhung der angegebenen positiven Zahl auf die angegebene Potenz darstellt.

## <a name="syntax"></a>Syntax

```vb
POWER (number, power)
```

## <a name="arguments"></a>Argumente

`number`: *Real* oder *Integer*

Ein numerischer Wert, der auf die angegebene Potenz angehoben werden muss.

`power`: *Real* oder *Integer*

Ein numerischer Wert, der die spezifische Potenz darstellt.

## <a name="return-values"></a>Rückgabewerte

*Gleitkommazahl*

Der resultierende numerische Wert.

## <a name="example-1"></a>Beispiel 1

`POWER (10, 2)` gibt **100** zurück.

## <a name="example-2"></a>Beispiel 2

`POWER (4, 0.5)` gibt **2** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Rechenoperationen](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]