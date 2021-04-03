---
title: DATETIMEFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETIMEFORMAT bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b7516620763e87440c0fb866ce507c744223a229
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563629"
---
# <a name="datetimeformat-er-function"></a><span data-ttu-id="3aec9-103">DATETIMEFORMAT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="3aec9-103">DATETIMEFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3aec9-104">Die Funktion `DATETIMEFORMAT` gibt den Wert *String* zurück, der einen vorgegebenen Wert für Datum/Uhrzeit als Text im angegebenen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt.</span><span class="sxs-lookup"><span data-stu-id="3aec9-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="3aec9-105">Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="3aec9-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="3aec9-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="3aec9-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="3aec9-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="3aec9-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="3aec9-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="3aec9-108">Arguments</span></span>

<span data-ttu-id="3aec9-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="3aec9-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="3aec9-110">Ein Datums-/Zeitwert, der das zu formatierende Datum und die Uhrzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="3aec9-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="3aec9-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="3aec9-111">`format`: *String*</span></span>

<span data-ttu-id="3aec9-112">Das Format der Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3aec9-112">The format of the output string.</span></span>

> [!NOTE]
> <span data-ttu-id="3aec9-113">Bei der Formatzeichenfolge wird zwischen Groß- und Kleinschreibung unterschieden, wenn Sie entweder ein Standardformat oder ein benutzerdefiniertes Format verwenden.</span><span class="sxs-lookup"><span data-stu-id="3aec9-113">The format string is case-sensitive when you use either a standard format or a custom format.</span></span> <span data-ttu-id="3aec9-114">Der [standardmäßige](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) Formatbezeichner „d“ gibt das Datum unter Verwendung des kurzen Datumsmusters zurück, während der Standardformatbezeichner „D“ das Datum unter Verwendung des langen Datumsmusters zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3aec9-114">For example, the [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) "d" format specifier returns the date by using the short date pattern, whereas the standard "D" format specifier returns the date by using the long date pattern.</span></span> <span data-ttu-id="3aec9-115">Darüber hinaus gibt der [benutzerdefinierte](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) Formatbezeichner „M“ den Monat von 1 bis 12 zurück, während der benutzerdefinierte Formatbezeichner „m“ die Minute von 0 bis 59 zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="3aec9-115">Additionally, the [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx) "M" format specifier returns the month from 1 through 12, whereas the custom "m" format specifier returns the minute from 0 through 59.</span></span>

<span data-ttu-id="3aec9-116">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="3aec9-116">`culture`: *String*</span></span>

<span data-ttu-id="3aec9-117">Die zum Formatieren zu verwendende Kultur.</span><span class="sxs-lookup"><span data-stu-id="3aec9-117">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="3aec9-118">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="3aec9-118">Return values</span></span>

<span data-ttu-id="3aec9-119">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="3aec9-119">*String*</span></span>

<span data-ttu-id="3aec9-120">Der resultierende Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="3aec9-120">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3aec9-121">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="3aec9-121">Usage notes</span></span>

<span data-ttu-id="3aec9-122">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert.</span><span class="sxs-lookup"><span data-stu-id="3aec9-122">If the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="3aec9-123">Wenn die Funktion `DATETIMEFORMAT` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="3aec9-123">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="3aec9-124">Der Standardwert `culture` lautet **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="3aec9-124">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="3aec9-125">Wenn die Funktion `DATETIMEFORMAT` einen bestimmten Datums-/Zeitwert konvertiert, berücksichtigt sie die Zeitzoneneinstellung des Anwendungsbenutzers, der das EB-Format ausführt, in dem die Funktion basierend auf dem Kontext abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3aec9-125">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="3aec9-126">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3aec9-126">Example 1</span></span>

<span data-ttu-id="3aec9-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum/die Uhrzeit des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format mit **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="3aec9-127">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="3aec9-128">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3aec9-128">Example 2</span></span>

<span data-ttu-id="3aec9-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` gibt das aktuelle Datum/den Zeitwert der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="3aec9-129">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="3aec9-130">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3aec9-130">Example 3</span></span>

<span data-ttu-id="3aec9-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` gibt den Zeichenkettenwert **2019-11-12T08:00:00.0000000-08:00** zurück, wenn die Funktion während eines Prozesses aufgerufen wird, der von einem Anwendungsbenutzer mit dem Zeitzonenwert **(GMT-08: 00) Pacific Time (USA und Kanada)** im Bereich **Sprach- und Länder-/Regionsvoreinstellungen** initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="3aec9-131">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when the function is called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3aec9-132">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="3aec9-132">Additional resources</span></span>

[<span data-ttu-id="3aec9-133">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="3aec9-133">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]