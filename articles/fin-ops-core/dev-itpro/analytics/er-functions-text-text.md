---
title: TEXT EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der TEXT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: bf9049463ca905952cab512884afad380b7b3d52
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8900163"
---
# <a name="text-er-function"></a>TEXT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `TEXT` gibt die angegebene Zahl mit dem Wert *String* zurück, nachdem sie in eine Textzeichenfolge konvertiert wurde, die gemäß den Servergebietsschemaeinstellungen der aktuellen Anwendungsinstanz formatiert ist.

## <a name="syntax"></a>Syntax

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumente

`number`: *Integer* oder *Real*

Eine Zahl, die in eine Textzeichenfolge konvertiert werden muss.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

Für Werte für den Typ *Real* wird die Zeichenkonvertierung auf zwei Dezimalstellen beschränkt.

## <a name="example"></a>Beispiel

Wenn das Servergebietsschema der Microsoft Dynamics 365 Finance-Instanz als **EN-US** definiert wird, gibt `TEXT (NOW ())` das aktuelle Finance-Sitzungsdatum, 17. Dezember 2015, als Textzeichenfolge **"12/17/2015 07:59:23 AM"** zurück. `TEXT (1/3)` gibt **"0.33"** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]