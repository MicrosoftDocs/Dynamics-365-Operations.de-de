---
title: OR EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der OR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 99b5ee37af1ea1a69985fb79b762b31561334fd6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268085"
---
# <a name="or-er-function"></a>OR EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `OR` gibt den *booleschen* Wert **FALSE** zurück, wenn alle angegebenen Bedingungen falsch sind. Wenn eine der angegebenen Bedingungen wahr ist, gibt die Funktion den *booleschen* Wert **TRUE** zurück.

## <a name="syntax"></a>Syntax

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a>Argumente

`condition 1`: *Boolesch*

Ein gültiger Bedingungsausdruck, der getestet werden muss. Dieses Argument ist erforderlich.

`condition N`: *Boolesch*

Ein gültiger Bedingungsausdruck, der getestet werden muss. Diese zusätzlichen Argumente sind optional.

## <a name="return-values"></a>Rückgabewerte

*Aktiv*

Der resultierende *boolesche* Wert.

## <a name="example"></a>Beispiel

`OR (1=2, "a"="a")` gibt **TRUE** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Logische Funktionen](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
