---
title: NEWGUID ER-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der NEWGUID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-09-08
ms.dyn365.ops.version: AX 10.0.23
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 381dbcbe816c189c1966ffe962020d5aa2b1f3eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9274771"
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
