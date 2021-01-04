---
title: NUMBERFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NUMBERFORMAT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 2c3907d1d2c74c852f4f90731e5f4bc23bfbd717
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680265"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="b1915-103">NUMBERFORMAT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="b1915-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1915-104">Die Funktion `NUMBERFORMAT` gibt den Wert *String* zurück, der eine angegebene Zahl im angegebenen Format und in einer optional angegebenen [Kultur](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1915-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](https://docs.microsoft.com/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="b1915-105">Informationen zu unterstützten Formaten finden Sie unter [Standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) und [Benutzerdefiniert](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="b1915-105">For information about the supported formats, see [standard](https://msdn.microsoft.com/library/dwhawy9k(v=vs.110).aspx) and [custom](https://msdn.microsoft.com/library/0c899ak8(v=vs.110).aspx).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="b1915-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="b1915-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="b1915-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="b1915-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="b1915-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="b1915-108">Arguments</span></span>

<span data-ttu-id="b1915-109">`number`: *Integer* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="b1915-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="b1915-110">Ein numerischer Wert, der die Nummer angibt, die formatiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b1915-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="b1915-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="b1915-111">`format` : *String*</span></span>

<span data-ttu-id="b1915-112">Der Wert *String*, der das Format darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1915-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="b1915-113">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="b1915-113">`culture`: *String*</span></span>

<span data-ttu-id="b1915-114">Der Wert *String*, der die für die Formatierung zu verwendende Kultur darstellt.</span><span class="sxs-lookup"><span data-stu-id="b1915-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="b1915-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b1915-115">Return values</span></span>

<span data-ttu-id="b1915-116">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="b1915-116">*String*</span></span>

<span data-ttu-id="b1915-117">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="b1915-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b1915-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="b1915-118">Usage notes</span></span>

<span data-ttu-id="b1915-119">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, bestimmt der Kontext, in dem diese Funktion ausgeführt wird, die Kultur, die zum Formatieren von Zahlen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1915-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="b1915-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b1915-120">Example 1</span></span>

<span data-ttu-id="b1915-121">Für die Kultur **EN-US** gibt `NUMBERFORMAT (0.45, "p")` **"45.00 %"** und `NUMBERFORMAT (10.45, "#")` **"10"** zurück.</span><span class="sxs-lookup"><span data-stu-id="b1915-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="b1915-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="b1915-122">Example 2</span></span>

<span data-ttu-id="b1915-123">`NUMBERFORMAT (10/3, "F2", "de")` gibt **3,33** zurück, wobei `NUMBERFORMAT (10/3, "F2", "en-us")` **3.33** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="b1915-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b1915-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b1915-124">Additional resources</span></span>

[<span data-ttu-id="b1915-125">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="b1915-125">Text functions</span></span>](er-functions-category-text.md)
