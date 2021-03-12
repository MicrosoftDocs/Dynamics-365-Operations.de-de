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
# <a name="dateformat-er-function"></a><span data-ttu-id="75415-103">DATEFORMAT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="75415-103">DATEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="75415-104">Die Funktion `DATEFORMAT` gibt den Wert *String* zurück, der einen vorgegebenen Datenwert als Text im angegebenen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt.</span><span class="sxs-lookup"><span data-stu-id="75415-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="75415-105">Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="75415-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="75415-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="75415-106">Syntax 1</span></span>

```vb
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="75415-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="75415-107">Syntax 2</span></span>

```vb
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="75415-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="75415-108">Arguments</span></span>

<span data-ttu-id="75415-109">`date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="75415-109">`date`: *Date*</span></span>

<span data-ttu-id="75415-110">Ein Datums-/Zeitwert, der das zu formatierende Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="75415-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="75415-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="75415-111">`format`: *String*</span></span>

<span data-ttu-id="75415-112">Das Format der Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="75415-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="75415-113">Bei der Formatzeichenfolge wird zwischen Groß- und Kleinschreibung unterschieden, wenn Sie entweder ein Standardformat oder ein benutzerdefiniertes Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="75415-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="75415-114">Der [standardmäßige](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) Formatbezeichner „d“ gibt das Datum unter Verwendung des kurzen Datumsmusters zurück, während der Standardformatbezeichner „D“ das Datum unter Verwendung des langen Datumsmusters zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="75415-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="75415-115">Darüber hinaus gibt der [benutzerdefinierte](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) Formatbezeichner „M“ den Monat von 1 bis 12 zurück, während der benutzerdefinierte Formatbezeichner „m“ die Minute von 0 bis 59 zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="75415-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="75415-116">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="75415-116">`culture`: *String*</span></span>

<span data-ttu-id="75415-117">Die zum Formatieren zu verwendende Kultur.</span><span class="sxs-lookup"><span data-stu-id="75415-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="75415-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="75415-118">Return values</span></span>

<span data-ttu-id="75415-119">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="75415-119">*String*</span></span>

<span data-ttu-id="75415-120">Der resultierende Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="75415-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="75415-121">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="75415-121">Usage notes</span></span>

<span data-ttu-id="75415-122">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert.</span><span class="sxs-lookup"><span data-stu-id="75415-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="75415-123">Wenn die Funktion `DATEFORMAT` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="75415-123">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="75415-124">Der Standardwert `culture` lautet **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="75415-124">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="75415-125">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="75415-125">Example 1</span></span>

<span data-ttu-id="75415-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format als Zeichenfolge **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="75415-126">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="75415-127">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="75415-127">Example 2</span></span>

<span data-ttu-id="75415-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` gibt das aktuelle Datum der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="75415-128">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="75415-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="75415-129">Additional resources</span></span>

[<span data-ttu-id="75415-130">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="75415-130">Date and time functions</span></span>](er-functions-category-datetime.md)
