---
title: DATETIMEFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETIMEFORMAT bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 01/04/2021
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
ms.openlocfilehash: 8044f81ee59af4a11bfab38525afdac5a46acd2c
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891256"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="f853e-103">DATETIMEFORMAT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="f853e-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f853e-104">Die Funktion `DATETIMEFORMAT` gibt den Wert *String* zurück, der einen vorgegebenen Wert für Datum/Uhrzeit als Text im angegebenen Format und in einer optional angegebenen [Kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt.</span><span class="sxs-lookup"><span data-stu-id="f853e-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="f853e-105">Informationen zu unterstützten Formaten finden Sie unter [Standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) und [Benutzerdefiniert](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="f853e-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) and [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="f853e-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="f853e-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="f853e-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="f853e-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="f853e-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="f853e-108">Arguments</span></span>

<span data-ttu-id="f853e-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="f853e-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="f853e-110">Ein Datums-/Zeitwert, der das zu formatierende Datum und die Uhrzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="f853e-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="f853e-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="f853e-111">`format`: *String*</span></span>

<span data-ttu-id="f853e-112">Das Format der Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="f853e-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="f853e-113">Bei der Formatzeichenfolge wird zwischen Groß- und Kleinschreibung unterschieden, wenn Sie entweder ein Standardformat oder ein benutzerdefiniertes Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="f853e-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="f853e-114">Der [standardmäßige](/dotnet/standard/base-types/standard-date-and-time-format-strings) Formatbezeichner „d“ gibt das Datum unter Verwendung des kurzen Datumsmusters zurück, während der Standardformatbezeichner „D“ das Datum unter Verwendung des langen Datumsmusters zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f853e-114">For example, the [standard](/dotnet/standard/base-types/standard-date-and-time-format-strings) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="f853e-115">Darüber hinaus gibt der [benutzerdefinierte](/dotnet/standard/base-types/custom-date-and-time-format-strings) Formatbezeichner „M“ den Monat von 1 bis 12 zurück, während der benutzerdefinierte Formatbezeichner „m“ die Minute von 0 bis 59 zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="f853e-115">Additionally, the [custom](/dotnet/standard/base-types/custom-date-and-time-format-strings) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="f853e-116">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="f853e-116">`culture`: *String*</span></span>

<span data-ttu-id="f853e-117">Die zum Formatieren zu verwendende Kultur.</span><span class="sxs-lookup"><span data-stu-id="f853e-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="f853e-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f853e-118">Return values</span></span>

<span data-ttu-id="f853e-119">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="f853e-119">*String*</span></span>

<span data-ttu-id="f853e-120">Der resultierende Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="f853e-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="f853e-121">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="f853e-121">Usage notes</span></span>

<span data-ttu-id="f853e-122">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert.</span><span class="sxs-lookup"><span data-stu-id="f853e-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="f853e-123">Wenn die Funktion `DATETIMEFORMAT` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="f853e-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="f853e-124">Der Standardwert `culture` lautet **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="f853e-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="f853e-125">Wenn die Funktion `DATETIMEFORMAT` einen bestimmten Datums-/Zeitwert konvertiert, berücksichtigt sie die Zeitzoneneinstellung des Anwendungsbenutzers, der das EB-Format ausführt, in dem die Funktion basierend auf dem Kontext abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f853e-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="f853e-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f853e-126">Example 1</span></span>

<span data-ttu-id="f853e-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum/die Uhrzeit des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format mit **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="f853e-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="f853e-128">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f853e-128">Example 2</span></span>

<span data-ttu-id="f853e-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` gibt das aktuelle Datum/den Zeitwert der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="f853e-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="f853e-130">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f853e-130">Example 3</span></span>

<span data-ttu-id="f853e-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` gibt den Zeichenkettenwert **2019-11-12T08:00:00.0000000-08:00** zurück, wenn die Funktion während eines Prozesses aufgerufen wird, der von einem Anwendungsbenutzer mit dem Zeitzonenwert **(GMT-08: 00) Pacific Time (USA und Kanada)** im Bereich **Sprach- und Länder-/Regionsvoreinstellungen** initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="f853e-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f853e-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f853e-132">Additional resources</span></span>

[<span data-ttu-id="f853e-133">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="f853e-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]