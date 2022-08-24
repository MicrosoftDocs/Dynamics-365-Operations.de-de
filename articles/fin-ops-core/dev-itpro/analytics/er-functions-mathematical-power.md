---
title: POWER EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der POWER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 9b6693d7c1afebcf9c30d1bf8d72950053c305bd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273994"
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
