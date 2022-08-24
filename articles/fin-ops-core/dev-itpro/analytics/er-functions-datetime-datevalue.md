---
title: DATEVALUE EB-Funktion
description: In diesem Artikel werden Informationen zur Verwendung der DATEVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: kfend
ms.date: 09/08/2021
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
ms.openlocfilehash: 290a4665d3527c0f0954c46cb0a0a14677b93218
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268697"
---
# <a name="datevalue-er-function"></a>DATEVALUE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `DATEVALUE` gibt den Wert *[Date](er-formula-supported-data-types-primitive.md#date)* zurück, der über einen vorgegebenen Textwert im speziellen Format und in einer optional angegebenen [Kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) in einen Datumswert konvertiert wird. Informationen zu unterstützten Formaten finden Sie unter [Standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) und [Benutzerdefiniert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntax 1

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntax 2

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumente

`text`: *[Zeichenfolge](er-formula-supported-data-types-primitive.md#string)*

Der Text, der den zu formatierenden Wert darstellt.

`format`: *String*

Das Format des angegebenen Textes. Informationen zu unterstützten Formaten finden Sie unter [Standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) und [Benutzerdefiniert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

`culture`: *String*

Die Kultur, die zum Formatieren des angegebenen Texts verwendet wird. Weitere Informationen zu unterstützten Kulturen finden Sie unter [Kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

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
