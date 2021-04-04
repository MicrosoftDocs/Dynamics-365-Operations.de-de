---
title: CHAR EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CHAR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: b008cf6ddf51d816a17e0fae1fa0db464adeabde
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563197"
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

Die Zeichenfolge, die diese Funktion zurückgibt, hängt von der Codierung ab, die im übergeordneten **DATEI**-Formatelement ausgewählt ist. Eine Liste der unterstützten Codierungen erhalten Sie unter [Codierungsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).

## <a name="example"></a>Beispiel

`CHAR (255)` gibt **"ÿ"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]