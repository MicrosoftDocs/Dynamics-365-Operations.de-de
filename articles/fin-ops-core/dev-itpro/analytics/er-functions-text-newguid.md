---
title: NEWGUID ER-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NEWGUID-Funktion bei der elektronischen Berichterstellung bereitgestellt.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: 5856a4d765f5136ecb11a34e0255c1ba88818f2c
ms.sourcegitcommit: 9e8d7536de7e1f01a3a707589f5cd8ca478d657b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 10/18/2021
ms.locfileid: "7647936"
---
# <a name="newguid-er-function"></a>NEWGUID ER-Funktion

[!include [banner](../includes/banner.md)]

Die `NEWGUID`-Funktion generiert einen neuen global eindeutigen Bezeichner (GUID) und gibt ihn als einen *[ GUID](er-formula-supported-data-types-primitive.md#guid)*-Wert zurück.

## <a name="syntax"></a>Syntax

```vb
NEWGUID ()
```

## <a name="return-values"></a>Rückgabewerte

*GUID*

Der resultierende GUID-Wert.

## <a name="example"></a>Beispiel

`NEWGUID()` gibt immer einen neuen *GUID*-Wert zurück, z. B. **3afcf7ff-af10-ec11-b6e6-000d3a13209e**.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
