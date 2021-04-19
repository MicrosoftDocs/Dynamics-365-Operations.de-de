---
title: DATEVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der DATEVALUE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: d760c3f874bfebad11b9497b136cb67df4e9ea61
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746938"
---
# <a name="datevalue-er-function"></a><span data-ttu-id="6d323-103">DATEVALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="6d323-103">DATEVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6d323-104">Die Funktion `DATEVALUE` gibt den Wert *Date* zurück, der über einen vorgegebenen Textwert im speziellen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) in einen Datumswert konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="6d323-104">The `DATEVALUE` function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) to a date value.</span></span> <span data-ttu-id="6d323-105">Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="6d323-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/az4se3k1(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/8kb3ddd4(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="6d323-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="6d323-106">Syntax 1</span></span>

```vb
DATEVALUE (text, format)
```

## <a name="syntax-2"></a><span data-ttu-id="6d323-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="6d323-107">Syntax 2</span></span>

```vb
DATEVALUE (text, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="6d323-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="6d323-108">Arguments</span></span>

<span data-ttu-id="6d323-109">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="6d323-109">`text`: *String*</span></span>

<span data-ttu-id="6d323-110">Der Text, der den zu formatierenden Wert darstellt.</span><span class="sxs-lookup"><span data-stu-id="6d323-110">Text that represents the value to format.</span></span>

<span data-ttu-id="6d323-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="6d323-111">`format`: *String*</span></span>

<span data-ttu-id="6d323-112">Das Format des angegebenen Textes.</span><span class="sxs-lookup"><span data-stu-id="6d323-112">The format of the given text.</span></span>

<span data-ttu-id="6d323-113">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="6d323-113">`culture`: *String*</span></span>

<span data-ttu-id="6d323-114">Die Kultur, die zum Formatieren des angegebenen Texts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d323-114">The culture that is used for formatting of the given text.</span></span>

## <a name="return-values"></a><span data-ttu-id="6d323-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6d323-115">Return values</span></span>

<span data-ttu-id="6d323-116">*Datum*</span><span class="sxs-lookup"><span data-stu-id="6d323-116">*Date*</span></span>

<span data-ttu-id="6d323-117">Der resultierende Datenwert.</span><span class="sxs-lookup"><span data-stu-id="6d323-117">The resulting date value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6d323-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="6d323-118">Usage notes</span></span>

<span data-ttu-id="6d323-119">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, wird der Wert `culture` durch den aufrufenden Kontext definiert.</span><span class="sxs-lookup"><span data-stu-id="6d323-119">When the culture isn't defined as an argument of the called function, the value of `culture` is defined by the calling context.</span></span> <span data-ttu-id="6d323-120">Wenn die Funktion `DATEVALUE` beispielsweise mit der Syntax 1 in einem EB-Format (elektronische Berichterstellung) für das Element **DATEI** abgerufen wird, das für die Verwendung der kulturspezifischen Kriterien für Deutschland konfiguriert ist, wird die Konvertierung unter Verwendung der kulturspezifischen Kriterien für Deutschland durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d323-120">For example, if the `DATEVALUE` function is called by using syntax 1 in an Electronic reporting (ER) format for a **FILE** element that is configured to use the German culture, the conversion will be done by using the German culture.</span></span> <span data-ttu-id="6d323-121">Der Standardwert `culture` lautet **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="6d323-121">The default `culture` value is **EN-US**.</span></span>

## <a name="example-1"></a><span data-ttu-id="6d323-122">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6d323-122">Example 1</span></span>

<span data-ttu-id="6d323-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` gibt den Datumswert **December 21, 2016** basierend auf dem angegebenen benutzerdefinierten Format und der Standardkultur **EN-US** der Anwendung zurück.</span><span class="sxs-lookup"><span data-stu-id="6d323-123">`DATEVALUE ("21-Dec-2016", "dd-MMM-yyyy")` returns the date value **December 21, 2016**, based on the specified custom format and the default application's **EN-US** culture.</span></span>

## <a name="example-2"></a><span data-ttu-id="6d323-124">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6d323-124">Example 2</span></span>

<span data-ttu-id="6d323-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` gibt den Datumswert **January 21, 2016** basierend auf dem angegebenen benutzerdefinierten Format und der Kultur zurück.</span><span class="sxs-lookup"><span data-stu-id="6d323-125">`DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "IT")` returns the date value **January 21, 2016**, based on the specified custom format and culture.</span></span>

<span data-ttu-id="6d323-126">Allerdings löst `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` eine Ausnahme aus, um den Benutzer zu informieren, dass die angegebene Zeichenfolge nicht als gültiger Wert für Datum/Uhrzeit für die angegebene Kultur anerkannt wird.</span><span class="sxs-lookup"><span data-stu-id="6d323-126">However, `DATEVALUE ("21-Gen-2016", "dd-MMM-yyyy", "EN-US")` throws an exception to inform the user that the specified string isn't recognized as a valid date for the specified culture.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6d323-127">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6d323-127">Additional resources</span></span>

[<span data-ttu-id="6d323-128">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="6d323-128">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]