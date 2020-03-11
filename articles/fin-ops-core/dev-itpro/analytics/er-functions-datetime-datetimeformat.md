---
title: DATETIMEFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETIMEFORMAT bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9e550b0c7634c7aac3f8c597a1c1eac3f8125e3b
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070712"
---
# <span data-ttu-id="0e38c-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="0e38c-103"><a name="DATETIMEFORMAT">DATETIMEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0e38c-104">Die Funktion `DATETIMEFORMAT` gibt den Wert *String* zurück, der einen vorgegebenen Wert für Datum/Uhrzeit als Text im angegebenen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e38c-104">The `DATETIMEFORMAT` function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="0e38c-105">(Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="0e38c-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="0e38c-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="0e38c-106">Syntax 1</span></span>

```vb
DATETIMEFORMAT (datetime, format)
```

## <a name="syntax-2"></a><span data-ttu-id="0e38c-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="0e38c-107">Syntax 2</span></span>

```vb
DATETIMEFORMAT (datetime, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="0e38c-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="0e38c-108">Arguments</span></span>

<span data-ttu-id="0e38c-109">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="0e38c-109">`datetime`: *DateTime*</span></span>

<span data-ttu-id="0e38c-110">Ein Datums-/Zeitwert, der das zu formatierende Datum und die Uhrzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="0e38c-110">A date/time value that represents the date and time to format.</span></span>

<span data-ttu-id="0e38c-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="0e38c-111">`format`: *String*</span></span>

<span data-ttu-id="0e38c-112">Das Format der Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0e38c-112">The format of the output string.</span></span>

<span data-ttu-id="0e38c-113">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="0e38c-113">`culture`: *String*</span></span>

<span data-ttu-id="0e38c-114">Die zum Formatieren zu verwendende Kultur.</span><span class="sxs-lookup"><span data-stu-id="0e38c-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="0e38c-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0e38c-115">Return values</span></span>

<span data-ttu-id="0e38c-116">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="0e38c-116">*String*</span></span>

<span data-ttu-id="0e38c-117">Der resultierende Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="0e38c-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0e38c-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="0e38c-118">Usage notes</span></span>

<span data-ttu-id="0e38c-119">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert.</span><span class="sxs-lookup"><span data-stu-id="0e38c-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="0e38c-120">Wenn die Funktion `DATETIMEFORMAT` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e38c-120">For example, if the `DATETIMEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="0e38c-121">Der Standardwert `culture` lautet **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="0e38c-121">The default `culture` value is **EN-US**.</span></span>

<span data-ttu-id="0e38c-122">Wenn die Funktion `DATETIMEFORMAT` einen bestimmten Datums-/Zeitwert konvertiert, berücksichtigt sie die Zeitzoneneinstellung des Anwendungsbenutzers, der das EB-Format ausführt, in dem die Funktion basierend auf dem Kontext abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0e38c-122">When the `DATETIMEFORMAT` function converts a given date/time value, it considers the time zone setting of the application user who is running the ER format that the function is called in the context of.</span></span>

## <a name="example-1"></a><span data-ttu-id="0e38c-123">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0e38c-123">Example 1</span></span>

<span data-ttu-id="0e38c-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum/die Uhrzeit des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format mit **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="0e38c-124">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="0e38c-125">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0e38c-125">Example 2</span></span>

<span data-ttu-id="0e38c-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` gibt das aktuelle Datum/den Zeitwert der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="0e38c-126">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="example-3"></a><span data-ttu-id="0e38c-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="0e38c-127">Example 3</span></span>

<span data-ttu-id="0e38c-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` gibt den Zeichenkettenwert **2019-11-12T08:00:00.0000000-08:00** zurück, wenn er während eines Prozesses aufgerufen wird, der von einem Anwendungsbenutzer mit dem Zeitzonenwert **(GMT-08: 00) Pacific Time (USA und Kanada)** im Bereich **Sprach- und Länder-/Regionsvoreinstellungen** initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="0e38c-128">`DATETIMEFORMAT (DATETIMEVALUE( "2019-11-12T09:00:00.0000000-07:00", "O"), "O")` returns the string value **2019-11-12T08:00:00.0000000-08:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT-08:00) Pacific Time (US & Canada)** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0e38c-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0e38c-129">Additional resources</span></span>

[<span data-ttu-id="0e38c-130">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="0e38c-130">Date and time functions</span></span>](er-functions-category-datetime.md)
