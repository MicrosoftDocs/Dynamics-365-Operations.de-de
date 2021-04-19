---
title: REPLACE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der REPLACE-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
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
ms.openlocfilehash: 21cdd8532730925b7d5c6f5b3bb565dcd365dd6d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746196"
---
# <a name="replace-er-function"></a><span data-ttu-id="49654-103">REPLACE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="49654-103">REPLACE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49654-104">Die Funktion `REPLACE` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er ganz oder teilweise durch eine andere Zeichenfolge ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="49654-104">The `REPLACE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="49654-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="49654-105">Syntax</span></span>

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a><span data-ttu-id="49654-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="49654-106">Arguments</span></span>

<span data-ttu-id="49654-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="49654-107">`text`: *String*</span></span>

<span data-ttu-id="49654-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="49654-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="49654-109">`pattern`: *String*</span><span class="sxs-lookup"><span data-stu-id="49654-109">`pattern`: *String*</span></span>

<span data-ttu-id="49654-110">Wenn das Argument `regular expression flag` **FALSE** lautet, enthält dieses Argument den Text, der ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="49654-110">If the `regular expression flag` argument is **FALSE**, this argument contains the text that must be replaced.</span></span>

<span data-ttu-id="49654-111">Wenn das Argument `regular expression flag` **TRUE** lautet, enthält dieses Argument einen regulären Ausdruck, der sowohl ein Suchmuster als auch den Ersetzungstext definiert.</span><span class="sxs-lookup"><span data-stu-id="49654-111">If the `regular expression flag` argument is **TRUE**, this argument contains a regular expression that defines both a search pattern and the replacement text.</span></span>

<span data-ttu-id="49654-112">`replacement`: *String*</span><span class="sxs-lookup"><span data-stu-id="49654-112">`replacement`: *String*</span></span>

<span data-ttu-id="49654-113">Wenn das Argument `regular expression flag` **FALSE** lautet, enthält dieses Argument den Text, der als Ersatz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="49654-113">If the `regular expression flag` argument is **FALSE**, this argument contains the text to use as a replacement.</span></span>

<span data-ttu-id="49654-114">Wenn das Argument `regular expression flag` **TRUE** lautet, wird dieses Argument nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="49654-114">If the `regular expression flag` argument is **TRUE**, this argument isn't used.</span></span>

<span data-ttu-id="49654-115">`regular expression flag`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="49654-115">`regular expression flag`: *Boolean*</span></span>

<span data-ttu-id="49654-116">Ein *boolescher* Wert, der angibt, ob ein regulärer Ausdruck zum Ersetzen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="49654-116">A *Boolean* value that indicates whether a regular expression is used to do the replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="49654-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="49654-117">Return values</span></span>

<span data-ttu-id="49654-118">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="49654-118">*String*</span></span>

<span data-ttu-id="49654-119">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="49654-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="49654-120">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="49654-120">Usage notes</span></span>

<span data-ttu-id="49654-121">Wenn das Argument `regular expression flag` **TRUE** lautet, gibt diese Funktion die angegebene Zeichenfolge zurück, nachdem sie geändert wurde, indem der reguläre Ausdruck angewendet wird, der durch das Argument `pattern` angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="49654-121">If the `regular expression flag` argument is **TRUE**, this function returns the specified string after it has been changed by applying the regular expression that is specified by the `pattern` argument.</span></span> <span data-ttu-id="49654-122">Der reguläre Ausdruck wird verwendet, um die Zeichen zu finden, die ersetzt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="49654-122">The regular expression is used to find the characters that must be replaced.</span></span>

<span data-ttu-id="49654-123">Wenn das Argument `regular expression flag` **FALSCH** ist, gibt die angegebene Zeichenfolge nach dem Zeichensatz zurück, der im Argument `pattern` Argument wurden durch Zeichen der ersetzt `replacement`Streit.</span><span class="sxs-lookup"><span data-stu-id="49654-123">If the `regular expression flag` argument is **FALSE**, this function returns the specified string after the set of characters that are defined in the `pattern` argument have been replaced by characters of the `replacement` argument.</span></span> 

## <a name="example-1"></a><span data-ttu-id="49654-124">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49654-124">Example 1</span></span>

<span data-ttu-id="49654-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` übernimmt einen regulären Ausdruck, der alle nicht numerischen Symbole entfernt und **"19234564971"** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="49654-125">`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` applies a regular expression that removes all non-numeric symbols, and it returns **"19234564971"**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="49654-126">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="49654-126">Example 2</span></span>

<span data-ttu-id="49654-127">`REPLACE ("abcdef", "cd", "GH", false)` ersetzt das Muster **"cd"** durch die Zeichenfolge **"GH"** und gibt **"abGHef"** zurück.</span><span class="sxs-lookup"><span data-stu-id="49654-127">`REPLACE ("abcdef", "cd", "GH", false)` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="49654-128">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="49654-128">Additional resources</span></span>

[<span data-ttu-id="49654-129">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="49654-129">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]