---
title: DATEVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der DATEVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 82feb8284f4b6116a53d174dcdd9b8c09c4fa63a
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563557"
---
# <a name="datevalue-er-function"></a>DATEVALUE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `DATEVALUE` gibt den Wert *Date* zurück, der über einen vorgegebenen Textwert im speziellen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) in einen Datumswert konvertiert wird. Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntax 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntax 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Text, der den zu formatierenden Wert darstellt.

`format`: *String*

Das Format des angegebenen Textes.

`culture`: *String*

Die Kultur, die zum Formatieren des angegebenen Texts verwendet wird.

## <a name="return-values"></a>Rückgabewerte

*Datum*

Der resultierende Datenwert.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert. Wenn die Funktion `DATEVALUE` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt. Der Standardwert `culture` lautet **EN-US**.

## <a name="example-1"></a>Beispiel 1

`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` gibt den Datumswert **December 21, 2016** basierend auf dem angegebenen benutzerdefinierten Format und der Standardkultur **EN-US** der Anwendung zurück.

## <a name="example-2"></a>Beispiel 2

`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` gibt den Datumswert **January 21, 2016** basierend auf dem angegebenen benutzerdefinierten Format und der Kultur zurück.

Allerdings löst `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` eine Ausnahme aus, um den Benutzer zu informieren, dass die angegebene Zeichenfolge nicht als gültiger Wert für Datum/Uhrzeit für die angegebene Kultur anerkannt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]