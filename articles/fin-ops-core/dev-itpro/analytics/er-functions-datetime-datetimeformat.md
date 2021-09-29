---
title: DATETIMEFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETIMEFORMAT bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 09/08/2021
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
ms.openlocfilehash: 1add2ccb348a9b518e0121be1184fbf6a684a0df
ms.sourcegitcommit: e7eeca05d738e9e46d6185d1ba349836ebafc1a4
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2021
ms.locfileid: "7485545"
---
# <a name="datetimeformat-er-function"></a>DATETIMEFORMAT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `DATETIMEFORMAT` gibt den Wert *[String](er-formula-supported-data-types-primitive.md#string)* zurück, der über einen vorgegebenen Zeitwert im speziellen Format und in einer optional angegebenen [Kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) einen vorgegebenen Datumswert darstellt. Informationen zu unterstützten Formaten finden Sie unter [Standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) und [Benutzerdefiniert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="syntax-1"></a>Syntax 1

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a>Syntax 2

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a>Argumente

`datetime`: *[DateTime](er-formula-supported-data-types-primitive.md#datetime)*

Ein Datums-/Zeitwert, der das zu formatierende Datum und die Uhrzeit darstellt.

`format`: *String*

Das Format der Ausgabezeichenfolge. Informationen zu unterstützten Formaten finden Sie unter [Standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) und [Benutzerdefiniert](/dotnet/standard/base-types/custom-date-and-time-format-strings).

> [!NOTE]
> Bei der Formatzeichenfolge wird zwischen Groß- und Kleinschreibung unterschieden, wenn Sie entweder ein Standardformat oder ein benutzerdefiniertes Format verwenden. Der [standardmäßige](/dotnet/standard/base-types/standard-date-and-time-format-strings) Formatbezeichner „d“ gibt das Datum unter Verwendung des kurzen Datumsmusters zurück, während der Standardformatbezeichner „D“ das Datum unter Verwendung des langen Datumsmusters zurückgibt. Darüber hinaus gibt der [benutzerdefinierte](/dotnet/standard/base-types/custom-date-and-time-format-strings) Formatbezeichner „M“ den Monat von 1 bis 12 zurück, während der benutzerdefinierte Formatbezeichner „m“ die Minute von 0 bis 59 zurückgibt.

`culture`: *String*

Die zum Formatieren zu verwendende Kultur. Weitere Informationen zu unterstützten Kulturen finden Sie unter [Kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Zeichenfolgenwert.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert. Wenn die Funktion `DATETIMEFORMAT` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt. Der Standardwert `culture` lautet **EN-US**.

Wenn die Funktion `DATETIMEFORMAT` einen bestimmten Datums-/Zeitwert konvertiert, berücksichtigt sie die Zeitzoneneinstellung des Anwendungsbenutzers, der das EB-Format ausführt, in dem die Funktion basierend auf dem Kontext abgerufen wird.

## <a name="example-1"></a>Beispiel 1

`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum/die Uhrzeit des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format mit **"24-12-2015"** zurück.

## <a name="example-2"></a>Beispiel 2

`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` gibt das aktuelle Datum/den Zeitwert der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.

## <a name="example-3"></a>Beispiel 3

`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` gibt den Zeichenkettenwert **2019-11-12T08:00:00.0000000-08:00** zurück, wenn die Funktion während eines Prozesses aufgerufen wird, der von einem Anwendungsbenutzer mit dem Zeitzonenwert **(GMT-08: 00) Pacific Time (USA und Kanada)** im Bereich **Sprach- und Länder-/Regionsvoreinstellungen** initiiert wird.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
