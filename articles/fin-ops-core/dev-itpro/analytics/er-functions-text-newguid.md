---
title: NEWGUID ER-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der NEWGUID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 321e2eda4accf9c8fe33b5a4c092c7be55276f26
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8861815"
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
