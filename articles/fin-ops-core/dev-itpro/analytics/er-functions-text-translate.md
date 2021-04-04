---
title: TRANSLATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von TRANSLATE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: f17d3439870710766906013e74452c2e76fec4ce
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560012"
---
# <a name="translate-er-function"></a><span data-ttu-id="ce375-103">TRANSLATE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="ce375-103">TRANSLATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce375-104">Die Funktion `TRANSLATE` gibt einen *Zeichenfolgen* Wert zurück, der das Ergebnis der Ersetzung des angegebenen Textes in Zeichen für einen anderen bereitgestellten Zeichensatz enthält.</span><span class="sxs-lookup"><span data-stu-id="ce375-104">The `TRANSLATE` function returns a *String* value that contains the result of the character replacement of specified text in characters of another provided set.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce375-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce375-105">Syntax</span></span>

```vb
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="ce375-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="ce375-106">Arguments</span></span>

<span data-ttu-id="ce375-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="ce375-107">`text`: *String*</span></span>

<span data-ttu-id="ce375-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="ce375-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="ce375-109">`pattern`: *String*</span><span class="sxs-lookup"><span data-stu-id="ce375-109">`pattern`: *String*</span></span>

<span data-ttu-id="ce375-110">Der Text, der ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="ce375-110">The text that must be replaced.</span></span>

<span data-ttu-id="ce375-111">`replacement`: *String*</span><span class="sxs-lookup"><span data-stu-id="ce375-111">`replacement`: *String*</span></span>

<span data-ttu-id="ce375-112">Den als Ersatz zu verwendenden Text.</span><span class="sxs-lookup"><span data-stu-id="ce375-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="ce375-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ce375-113">Return values</span></span>

<span data-ttu-id="ce375-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="ce375-114">*String*</span></span>

<span data-ttu-id="ce375-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="ce375-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ce375-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="ce375-116">Usage notes</span></span>

<span data-ttu-id="ce375-117">Die `TRANSLATE` Funktion ersetzt jeweils ein Zeichen.</span><span class="sxs-lookup"><span data-stu-id="ce375-117">The `TRANSLATE` function replaces one character at a time.</span></span> <span data-ttu-id="ce375-118">Die Funktion ersetzt das erste Zeichen des `text` Arguments mit dem ersten Zeichen des `pattern` Arguments und dann das zweite Zeichen und folgt dem gleichen Ablauf bis zum Ende.</span><span class="sxs-lookup"><span data-stu-id="ce375-118">The function replaces the first character of the `text` argument with the first character of the `pattern` argument and then the second character and follows the same flow until finished.</span></span> <span data-ttu-id="ce375-119">Wenn ein Charakter aus dem `text` und `pattern` Argumente übereinstimmt, wird es durch ein Zeichen aus dem Argument `replacement` ersetzt, das sich an derselben Position befindet wie das Zeichen aus dem Argument `pattern`.</span><span class="sxs-lookup"><span data-stu-id="ce375-119">When a character from the `text` and `pattern` arguments match, it is replaced by a character from the `replacement` argument that is located in the same position as the character from the `pattern` argument.</span></span> <span data-ttu-id="ce375-120">Wenn ein Zeichen mehrmals im Argument `pattern` angezeigt wird, wird das Argument `replacement`, das dem ersten Auftreten dieses Zeichens entspricht, zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ce375-120">If a character appears multiple times in the `pattern` argument, the `replacement` argument mapping that corresponds to the first occurrence of this character is used.</span></span>

## <a name="example-1"></a><span data-ttu-id="ce375-121">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ce375-121">Example 1</span></span>

<span data-ttu-id="ce375-122">`TRANSLATE ("abcdef", "cd", "GH")` ersetzt das Zeichen **c** des angegebenen **abcdef** Texts mit dem **G** Zeichen der `replacement` Texts aus folgenden Gründen:</span><span class="sxs-lookup"><span data-stu-id="ce375-122">`TRANSLATE ("abcdef", "cd", "GH")` replaces the **"c"** character of the specified  **“abcdef”** text with the **"G"** character of the `replacement` text due to the following:</span></span>
-   <span data-ttu-id="ce375-123">Das Zeichen **c** wird im dargestellten Text `pattern` an der ersten Stelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ce375-123">The **"c"** character is presented in the `pattern` text in the first position.</span></span>
-   <span data-ttu-id="ce375-124">Die erste Position des Texts `replacement` enthält das Zeichen **G**.</span><span class="sxs-lookup"><span data-stu-id="ce375-124">The first position of the `replacement` text contains the **"G"** character.</span></span>

## <a name="example-2"></a><span data-ttu-id="ce375-125">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ce375-125">Example 2</span></span>

<span data-ttu-id="ce375-126">`TRANSLATE ("abcdef", "ccd", "GH")` gibt **abcdef** zurück.</span><span class="sxs-lookup"><span data-stu-id="ce375-126">`TRANSLATE ("abcdef", "ccd", "GH")` returns **"abGdef"**.</span></span>

## <a name="example-3"></a><span data-ttu-id="ce375-127">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ce375-127">Example 3</span></span>

<span data-ttu-id="ce375-128">`TRANSLATE ("abccba", "abc", "123")` gibt **"123321"** zurück.</span><span class="sxs-lookup"><span data-stu-id="ce375-128">`TRANSLATE ("abccba", "abc", "123")` returns **"123321"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce375-129">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ce375-129">Additional resources</span></span>

[<span data-ttu-id="ce375-130">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="ce375-130">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]