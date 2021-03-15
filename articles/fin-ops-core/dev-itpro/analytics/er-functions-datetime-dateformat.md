---
title: DATEFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der DATEFORMAT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 01/04/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: cdc1671f818bc2c4d8a78d0a35337298e83c5060
ms.sourcegitcommit: 7cfe8931dd454e811a691f5118a4ecae7ba4b478
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/04/2021
ms.locfileid: "4826010"
---
# <a name="dateformat-er-function"></a>DATEFORMAT EB-Funktion

[!include [banner](../includes/banner.md)]

Die Funktion `DATEFORMAT` gibt den Wert *String* zurück, der einen vorgegebenen Datenwert als Text im angegebenen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt. Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).

## <a name="syntax-1"></a>Syntax 1

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a>Syntax 2

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a>Argumente

`date`: *Date*

Ein Datums-/Zeitwert, der das zu formatierende Datum darstellt.

`format`: *String*

Das Format der Ausgabezeichenfolge.

> [!NOTE]
> Bei der Formatzeichenfolge wird zwischen Groß- und Kleinschreibung unterschieden, wenn Sie entweder ein Standardformat oder ein benutzerdefiniertes Format verwenden. Der [standardmäßige](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) Formatbezeichner „d“ gibt das Datum unter Verwendung des kurzen Datumsmusters zurück, während der Standardformatbezeichner „D“ das Datum unter Verwendung des langen Datumsmusters zurückgibt. Darüber hinaus gibt der [benutzerdefinierte](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) Formatbezeichner „M“ den Monat von 1 bis 12 zurück, während der benutzerdefinierte Formatbezeichner „m“ die Minute von 0 bis 59 zurückgibt.

`culture`: *String*

Die zum Formatieren zu verwendende Kultur.

## <a name="return-values"></a>Rückgabewerte

*Zeichenfolge*

Der resultierende Zeichenfolgenwert.

## <a name="usage-notes"></a>Anwendungshinweise

Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert. Wenn die Funktion `DATEFORMAT` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt. Der Standardwert `culture` lautet **EN-US**.

## <a name="example-1"></a>Beispiel 1

`DATEFORMAT (TODAY (), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format als Zeichenfolge **"24-12-2015"** zurück.

## <a name="example-2"></a>Beispiel 2

`DATEFORMAT (SESSIONTODAY (), "d", "DE")` gibt das aktuelle Datum der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.

## <a name="additional-resources"></a>Zusätzliche Ressourcen

[Datums- und Zeitfunktionen](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]