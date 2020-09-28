---
title: TRANSLATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von TRANSLATE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: 51b9a2e25a9f1dfc08e9e0f7fc3ad84b359a6d1b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744238"
---
# <a name="translate-er-function"></a><span data-ttu-id="ae2e8-103">TRANSLATE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="ae2e8-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae2e8-104">Die Funktion `TRANSLATE` gibt einen *Zeichenfolgen* Wert zurück, der das Ergebnis der Ersetzung des angegebenen Textes in Zeichen für einen anderen bereitgestellten Zeichensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae2e8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae2e8-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="ae2e8-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="ae2e8-106">Arguments</span></span>

<span data-ttu-id="ae2e8-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="ae2e8-107">`text`: *String*</span></span>

<span data-ttu-id="ae2e8-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="ae2e8-109">`pattern`: *String*</span><span class="sxs-lookup"><span data-stu-id="ae2e8-109">`pattern`: *String*</span></span>

<span data-ttu-id="ae2e8-110">Der Text, der ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-110">The text that must be replaced.</span></span>

<span data-ttu-id="ae2e8-111">`replacement`: *String*</span><span class="sxs-lookup"><span data-stu-id="ae2e8-111">`replacement`: *String*</span></span>

<span data-ttu-id="ae2e8-112">Den als Ersatz zu verwendenden Text.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="ae2e8-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ae2e8-113">Return values</span></span>

<span data-ttu-id="ae2e8-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="ae2e8-114">*String*</span></span>

<span data-ttu-id="ae2e8-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ae2e8-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="ae2e8-116">Usage notes</span></span>

<span data-ttu-id="ae2e8-117">Die `TRANSLATE` Funktion ersetzt jeweils ein Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="ae2e8-118">Die Funktion ersetzt das erste Zeichen des `text` Arguments mit dem ersten Zeichen des `pattern` Arguments und dann das zweite Zeichen und folgt dem gleichen Ablauf bis zum Ende.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="ae2e8-119">Wenn ein Charakter aus dem `text` und `pattern` Argumente übereinstimmt, wird es durch ein Zeichen aus dem Argument `replacement` ersetzt, das sich an derselben Position befindet wie das Zeichen aus dem Argument `pattern`.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="ae2e8-120">Wenn ein Zeichen mehrmals im Argument `pattern` angezeigt wird, wird das Argument `replacement`, das dem ersten Auftreten dieses Zeichens entspricht, zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="ae2e8-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae2e8-121">Example 1</span></span>

<span data-ttu-id="ae2e8-122">`TRANSLATE ("abcdef", "cd", "GH")` ersetzt das Zeichen **c** des angegebenen **abcdef** Texts mit dem **G** Zeichen der `replacement` Texts aus folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="ae2e8-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="ae2e8-123">Das Zeichen **c** wird im dargestellten Text `pattern` an der ersten Stelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="ae2e8-124">Die erste Position des Texts `replacement` enthält das Zeichen **G**.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="ae2e8-125">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ae2e8-125">Example 2</span></span>

<span data-ttu-id="ae2e8-126">`TRANSLATE ("abcdef", "ccd", "GH")` gibt **abcdef** zurück.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="ae2e8-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ae2e8-127">Example 3</span></span>

<span data-ttu-id="ae2e8-128">`TRANSLATE ("abccba", "abc", "123")` gibt **"123321"** zurück.</span><span class="sxs-lookup"><span data-stu-id="ae2e8-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ae2e8-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ae2e8-129">Additional resources</span></span>

[<span data-ttu-id="ae2e8-130">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="ae2e8-130">Text functions</span></span>](er-functions-category-text.md)
