---
title: ABS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ABS-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565783"
---
# <a name="abs-er-function"></a>ABS EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `ABS` gibt den absoluten Wert (Modulus) der angegebenen Zahl mit dem Wert *Real* zurück. In anderen Worten gibt sie die Zahl ohne das Vorzeichen zurück.

## <a name="syntax"></a>Syntax

```vb
ABS (number)
```

## <a name="arguments"></a>Argumente

`number`: *Real*

Ein numerischer Wert, dessen Modul Sie verwenden möchten.

## <a name="return-values"></a>Rückgabewerte

*Gleitkommazahl*

Der resultierende numerische Wert.

## <a name="example"></a>Beispiel

`ABS (-1)` gibt **1** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Rechenoperationen](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]