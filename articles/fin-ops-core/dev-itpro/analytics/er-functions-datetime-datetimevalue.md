---
title: DATETIMEVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETIMEVALUE bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: 29d81599563dec2827fa8a82c86b74cb9e34eea2
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070689"
---
# <span data-ttu-id="4d57c-103"><a name="DATETIMEVALUE">DATETIMEVALUE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="4d57c-103"><a name="DATETIMEVALUE">DATETIMEVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4d57c-104">Die Funktion `DATETIMEVALUE` gibt den Wert *DateTime* zurück, der über einen vorgegebenen Textwert in das spezielle Format und in eine optional angegebene [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) in einen Wert für Datum/Uhrzeit konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="4d57c-104">The `DATETIMEVALUE` function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date/time value.</span></span> <span data-ttu-id="4d57c-105">(Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="4d57c-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="4d57c-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="4d57c-106">Syntax 1</span></span>

```vb
DATETIMEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="4d57c-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="4d57c-107">Syntax 2</span></span>

```vb
DATETIMEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="4d57c-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="4d57c-108">Arguments</span></span>

<span data-ttu-id="4d57c-109">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="4d57c-109">`text`: *String*</span></span>

<span data-ttu-id="4d57c-110">Der Text, der den zu formatierenden Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="4d57c-110">Text that represents the value to format.</span></span>

<span data-ttu-id="4d57c-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="4d57c-111">`format`: *String*</span></span>

<span data-ttu-id="4d57c-112">Das Format des angegebenen Textes.</span><span class="sxs-lookup"><span data-stu-id="4d57c-112">The format of the given text.</span></span>

<span data-ttu-id="4d57c-113">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="4d57c-113">`culture`: *String*</span></span>

<span data-ttu-id="4d57c-114">Die Kultur, die zum Formatieren des angegebenen Texts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d57c-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="4d57c-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4d57c-115">Return values</span></span>

<span data-ttu-id="4d57c-116">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="4d57c-116">*DateTime*</span></span>

<span data-ttu-id="4d57c-117">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="4d57c-117">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4d57c-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="4d57c-118">Usage notes</span></span>

<span data-ttu-id="4d57c-119">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert.</span><span class="sxs-lookup"><span data-stu-id="4d57c-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="4d57c-120">Wenn die Funktion `DATETIMEVALUE` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d57c-120">For example, if the `DATETIMEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="4d57c-121">Der Standardwert `culture` lautet **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="4d57c-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="4d57c-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d57c-122">Example 1</span></span>

<span data-ttu-id="4d57c-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` gibt **2:55:00 AM on December 21, 2016** basierend auf dem angegebenen benutzerdefinierten Format und der Standardkultur **EN-US** der Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="4d57c-123">`DATETIMEVALUE ("21-Dec-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="4d57c-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4d57c-124">Example 2</span></span>

<span data-ttu-id="4d57c-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` gibt **2:55:00 AM on December 21, 2016** basierend auf dem angegebenen benutzerdefinierten Format und der Kultur zurück.</span><span class="sxs-lookup"><span data-stu-id="4d57c-125">`DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "IT")` returns **2:55:00 AM on December 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="4d57c-126">Allerdings löst `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` eine Ausnahme aus, um den Benutzer zu informieren, dass die angegebene Zeichenfolge nicht als gültiger Wert für Datum/Uhrzeit für die angegebene Kultur anerkannt wird.</span><span class="sxs-lookup"><span data-stu-id="4d57c-126">However, `DATETIMEVALUE ("21-Gen-2016 02:55:00", "dd-MMM-yyyy hh:mm:ss", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date/time value for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4d57c-127">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4d57c-127">Additional resources</span></span>

[<span data-ttu-id="4d57c-128">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="4d57c-128">Date and time functions</span></span>](er-functions-category-datetime.md)
