---
title: CHAR EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CHAR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: e422ccc406e919b2191f4bccb1ac8198bba84b09e9f01f6971876e2c6507d6d3
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/05/2021
ms.locfileid: "6754365"
---
# <a name="char-er-function"></a>CHAR EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `CHAR` gibt den Wert *String* zurück, der ein einzelnes Zeichen darstellt, auf das durch die angegebene Unicode-Nummer verwiesen wird.

## <a name="syntax"></a>Syntax

```vb
CHAR (number)
```

## <a name="arguments"></a>Argumente

`number`: *Integer*

Eine Zahl, die einem erwarteten einzelnen Zeichen entspricht.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Die Zeichenfolge, die diese Funktion zurückgibt, hängt von der Codierung ab, die im übergeordneten **DATEI**-Formatelement ausgewählt ist. Eine Liste der unterstützten Codierungen erhalten Sie unter [Codierungsklasse](/dotnet/api/system.text.encoding).

## <a name="example"></a>Beispiel

`CHAR (255)` gibt **"ÿ"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]