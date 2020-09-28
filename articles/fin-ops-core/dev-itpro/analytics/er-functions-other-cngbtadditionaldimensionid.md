---
title: CN_GBT_ADDITIONALDIMENSIONID EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CN_GBT_ADDITIONALDIMENSIONID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fdc4527bc6115bdb3fca9d6a92d3d77a7c264c2
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744430"
---
# <a name="cn_gbt_additionaldimensionid-er-function"></a>CN_GBT_ADDITIONALDIMENSIONID EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `CN_GBT_ADDITIONALDIMENSIONID` gibt den Wert *String* zurück, der eine einzelne Finanzdimensions-ID darstellt, die der angegebenen Zeichenfolge entnommen wird. Die angegebene Zeichenfolge zeigt alle Dimensionen als durch Kommata getrennte ID-Listen an.

## <a name="syntax"></a>Syntax

```vb
CN_GBT_ADDITIONALDIMENSIONID (text, number)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Wert *String* zeigt alle Dimensionen als durch Kommata getrennte ID-Listen an.

`number`: Integer

Der Wert *Integer*, der den Sequenzcode der gewünschten Dimension in der angegebenen Zeichenfolge definiert.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="example"></a>Beispiel

`CN_GBT_AdditionalDimensionID ("AA,BB,CC,DD,EE,FF,GG,HH", 3)` gibt **"CC"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Andere (geschäftsdomänenspezifische) Funktionen](er-functions-category-other.md)
