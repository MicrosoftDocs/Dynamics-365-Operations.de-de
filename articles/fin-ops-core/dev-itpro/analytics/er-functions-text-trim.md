---
title: TRIM EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der TRIM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: deadf89641771efa864e701af9dad57c5e62ea37
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864643"
---
# <a name="trim-er-function"></a>TRIM EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `TRIM` gibt die angegebene Textzeichenfolge als *String* zurück, nachdem Tabulator-, Wagenrücklauf-, Zeilenvorschub- und Formularvorschubzeichen durch ein einzelnes Leerzeichen ersetzt wurden, nachdem führende und nachfolgende Leerzeichen abgeschnitten wurden und nachdem mehrere Leerzeichen zwischen Wörtern entfernt wurden.

## <a name="syntax"></a>Syntax

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der gültige Pfad einer Datenquelle des Typs *String*.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Textwert.

## <a name="usage-notes"></a>Anwendungshinweise

In einigen Fällen möchten Sie vielleicht führende und nachgestellte Leerzeichen abschneiden, aber die Formatierung des angegebenen Textes beibehalten. Zum Beispiel, wenn dieser Text eine Adresse darstellt, die in das mehrzeilige Textfeld eingegeben werden kann und Zeilenvorschub- und Wagenrücklaufformatierungen enthalten kann. Verwenden Sie in diesem Fall den folgenden Ausdruck: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)`, wobei `text` das Argument ist, das sich auf die angegebene Textzeichenfolge bezieht.

## <a name="example-1"></a>Beispiel 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` gibt **"Sample text"** zurück.

## <a name="example-2"></a>Beispiel 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` gibt **„Sample text“** zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Textfunktionen](er-functions-category-text.md)

[REPLACE EB-Funktion](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
