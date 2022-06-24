---
title: OR EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der OR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: d2783b5aff34e6ab4b5bde5dfe39e92d20892634
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892950"
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