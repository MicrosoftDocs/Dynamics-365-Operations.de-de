---
title: DATEFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der DATEFORMAT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: c1453be0c93764f9f0364206822a9e3899061a58
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917579"
---
# <span data-ttu-id="ca2d5-103"><a name="DATEFORMAT">DATEFORMAT EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="ca2d5-103"><a name="DATEFORMAT">DATEFORMAT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ca2d5-104">Die Funktion `DATEFORMAT` gibt den Wert *String* zurück, der einen vorgegebenen Datenwert als Text im angegebenen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-104">The `DATEFORMAT` function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="ca2d5-105">(Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="ca2d5-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="ca2d5-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="ca2d5-106">Syntax 1</span></span>

```
DATEFORMAT (date, format)
```

## <a name="syntax-2"></a><span data-ttu-id="ca2d5-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="ca2d5-107">Syntax 2</span></span>

```
DATEFORMAT (date, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="ca2d5-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="ca2d5-108">Arguments</span></span>

<span data-ttu-id="ca2d5-109">`date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="ca2d5-109">`date`: *Date*</span></span>

<span data-ttu-id="ca2d5-110">Ein Datums-/Zeitwert, der das zu formatierende Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-110">A date value that represents the date to format.</span></span>

<span data-ttu-id="ca2d5-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="ca2d5-111">`format`: *String*</span></span>

<span data-ttu-id="ca2d5-112">Das Format der Ausgabezeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-112">The format of the output string.</span></span>

<span data-ttu-id="ca2d5-113">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="ca2d5-113">`culture`: *String*</span></span>

<span data-ttu-id="ca2d5-114">Die zum Formatieren zu verwendende Kultur.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-114">The culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="ca2d5-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ca2d5-115">Return values</span></span>

<span data-ttu-id="ca2d5-116">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="ca2d5-116">*String*</span></span>

<span data-ttu-id="ca2d5-117">Der resultierende Zeichenfolgenwert.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-117">The resulting string value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ca2d5-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="ca2d5-118">Usage notes</span></span>

<span data-ttu-id="ca2d5-119">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="ca2d5-120">Wenn die Funktion `DATEFORMAT` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-120">For example, if the `DATEFORMAT` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="ca2d5-121">Der Standardwert `culture` lautet **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="ca2d5-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ca2d5-122">Example 1</span></span>

<span data-ttu-id="ca2d5-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format als Zeichenfolge **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-123">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="ca2d5-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ca2d5-124">Example 2</span></span>

<span data-ttu-id="ca2d5-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` gibt das aktuelle Datum der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="ca2d5-125">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string  **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca2d5-126">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ca2d5-126">Additional resources</span></span>

[<span data-ttu-id="ca2d5-127">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="ca2d5-127">Date and time functions</span></span>](er-functions-category-datetime.md)