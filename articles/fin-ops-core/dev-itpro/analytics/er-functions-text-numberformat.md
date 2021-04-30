---
title: NUMBERFORMAT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NUMBERFORMAT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/10/2019
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
ms.openlocfilehash: 4a383b3f7c0ca7c4e5afc609cc8a7b1b07021b02
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890382"
---
# <a name="numberformat-er-function"></a><span data-ttu-id="8db06-103">NUMBERFORMAT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="8db06-103">NUMBERFORMAT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8db06-104">Die Funktion `NUMBERFORMAT` gibt den Wert *String* zurück, der eine angegebene Zahl im angegebenen Format und in einer optional angegebenen [Kultur](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes) darstellt.</span><span class="sxs-lookup"><span data-stu-id="8db06-104">The `NUMBERFORMAT` function returns a *String* value that presents the specified number in the specified format and in an optionally specified [culture](/bingmaps/rest-services/common-parameters-and-types/supported-culture-codes).</span></span> <span data-ttu-id="8db06-105">Informationen zu unterstützten Formaten finden Sie unter [Standard](/dotnet/standard/base-types/standard-numeric-format-strings) und [Benutzerdefiniert](/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="8db06-105">For information about the supported formats, see [standard](/dotnet/standard/base-types/standard-numeric-format-strings) and [custom](/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="syntax-1"></a><span data-ttu-id="8db06-106">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="8db06-106">Syntax 1</span></span>

```vb
NUMBERFORMAT (number, format)
```

## <a name="syntax-2"></a><span data-ttu-id="8db06-107">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="8db06-107">Syntax 2</span></span>

```vb
NUMBERFORMAT (number, format, culture)
```

## <a name="arguments"></a><span data-ttu-id="8db06-108">Argumente</span><span class="sxs-lookup"><span data-stu-id="8db06-108">Arguments</span></span>

<span data-ttu-id="8db06-109">`number`: *Integer* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="8db06-109">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="8db06-110">Ein numerischer Wert, der die Nummer angibt, die formatiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="8db06-110">A numeric value that specifies the number that must be formatted.</span></span>

<span data-ttu-id="8db06-111">`format`: *String*</span><span class="sxs-lookup"><span data-stu-id="8db06-111">`format` : *String*</span></span>

<span data-ttu-id="8db06-112">Der Wert *String*, der das Format darstellt.</span><span class="sxs-lookup"><span data-stu-id="8db06-112">A *String* value that represents the format.</span></span>

<span data-ttu-id="8db06-113">`culture`: *String*</span><span class="sxs-lookup"><span data-stu-id="8db06-113">`culture`: *String*</span></span>

<span data-ttu-id="8db06-114">Der Wert *String*, der die für die Formatierung zu verwendende Kultur darstellt.</span><span class="sxs-lookup"><span data-stu-id="8db06-114">A *String* value that represents the culture to use for formatting.</span></span>

## <a name="return-values"></a><span data-ttu-id="8db06-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8db06-115">Return values</span></span>

<span data-ttu-id="8db06-116">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="8db06-116">*String*</span></span>

<span data-ttu-id="8db06-117">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="8db06-117">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8db06-118">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="8db06-118">Usage notes</span></span>

<span data-ttu-id="8db06-119">Wenn die Kultur nicht als Argument der aufgerufenen Funktion definiert ist, bestimmt der Kontext, in dem diese Funktion ausgeführt wird, die Kultur, die zum Formatieren von Zahlen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8db06-119">If the culture isn't defined as an argument of the called function, the context that this function is run in determines the culture that is used to format numbers.</span></span>

## <a name="example-1"></a><span data-ttu-id="8db06-120">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8db06-120">Example 1</span></span>

<span data-ttu-id="8db06-121">Für die Kultur **EN-US** gibt `NUMBERFORMAT (0.45, "p")` **"45.00 %"** und `NUMBERFORMAT (10.45, "#")` **"10"** zurück.</span><span class="sxs-lookup"><span data-stu-id="8db06-121">For the **EN-US** culture, `NUMBERFORMAT (0.45, "p")` returns **"45.00 %"**, and `NUMBERFORMAT (10.45, "#")` returns **"10"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="8db06-122">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8db06-122">Example 2</span></span>

<span data-ttu-id="8db06-123">`NUMBERFORMAT (10/3, "F2", "de")` gibt **3,33** zurück, wobei `NUMBERFORMAT (10/3, "F2", "en-us")` **3.33** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="8db06-123">`NUMBERFORMAT (10/3, "F2", "de")` returns **3,33**, whereas `NUMBERFORMAT (10/3, "F2", "en-us")` returns **3.33**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8db06-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="8db06-124">Additional resources</span></span>

[<span data-ttu-id="8db06-125">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="8db06-125">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]