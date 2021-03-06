---
title: DATETIMEVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETIMEVALUE bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: db5b2c56f0c6dcc019419801821d7a6eae8a0e91
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891280"
---
# <a name="datetimevalue-er-function"></a>DATETIMEVALUE EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `DATETIMEVALUE` gibt den Wert *DateTime* zurück, der über einen vorgegebenen Textwert in das spezielle Format und in eine optional angegebene [Kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) in einen Wert für Datum/Uhrzeit konvertiert wird. Informationen zu unterstützten Formaten finden Sie unter [Standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) und [Benutzerdefiniert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntax 1

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a>Syntax 2

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a>Argumente

`text`: *String*

Der Text, der den zu formatierenden Wert darstellt.

`format`: *String*

Das Format des angegebenen Textes.

`culture`: *String*

Die Kultur, die zum Formatieren des angegebenen Texts verwendet wird.

## <a name="return-values"></a>Rückgabewerte

*DateTime*

Der resultierende Wert für Datum/Uhrzeit.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert. Wenn die Funktion `DATETIMEVALUE` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt. Der Standardwert `culture` lautet **EN-US**.

## <a name="example-1"></a>Beispiel 1

`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` gibt **2:55:00 AM on December 21, 2016** basierend auf dem angegebenen benutzerdefinierten Format und der Standardkultur **EN-US** der Anwendung zurück.

## <a name="example-2"></a>Beispiel 2

`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` gibt **2:55:00 AM on December 21, 2016** basierend auf dem angegebenen benutzerdefinierten Format und der Kultur zurück.

Allerdings löst `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` eine Ausnahme aus, um den Benutzer zu informieren, dass die angegebene Zeichenfolge nicht als gültiger Wert für Datum/Uhrzeit für die angegebene Kultur anerkannt wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]