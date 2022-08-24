---
title: TRIM EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der TRIM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 02/28/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273097"
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
