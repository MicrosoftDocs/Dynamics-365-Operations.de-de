---
title: NUMERALSTOTEXT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der NUMERALSTOTEXT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: e4af3926998d128f8269ab9af46caeb8be896509
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680217"
---
# <a name="numeralstotext-er-function"></a><span data-ttu-id="d3068-103">NUMERALSTOTEXT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="d3068-103">NUMERALSTOTEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3068-104">Die Funktion `NUMERALSTOTEXT` gibt die angegebene Zahl mit dem Wert *String* zurück, nachdem er in der angegebenen Sprache geschrieben (d. h. in Textzeichenfolgen konvertiert) wurde.</span><span class="sxs-lookup"><span data-stu-id="d3068-104">The `NUMERALSTOTEXT` function returns the specified number as a *String* value after it has been spelled out (that is, converted to text strings) in the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3068-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3068-105">Syntax</span></span>

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a><span data-ttu-id="d3068-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="d3068-106">Arguments</span></span>

<span data-ttu-id="d3068-107">`number`: *Integer* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="d3068-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="d3068-108">Ein numerischer Wert, der die Nummer angibt, die ausgeschrieben werden muss.</span><span class="sxs-lookup"><span data-stu-id="d3068-108">A numeric value that specifies the number that must be spelled out.</span></span>

<span data-ttu-id="d3068-109">`language`: *String*</span><span class="sxs-lookup"><span data-stu-id="d3068-109">`language`: *String*</span></span>

<span data-ttu-id="d3068-110">Der Wert *String*, der den Sprachcode darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3068-110">A *String* value that represents the language code.</span></span>

<span data-ttu-id="d3068-111">`currency`: *String*</span><span class="sxs-lookup"><span data-stu-id="d3068-111">`currency`: *String*</span></span>

<span data-ttu-id="d3068-112">Der Wert *String*, der den Währungscode darstellt.</span><span class="sxs-lookup"><span data-stu-id="d3068-112">A *String* value that represents the currency code.</span></span>

<span data-ttu-id="d3068-113">`print currency name flag`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="d3068-113">`print currency name flag`: *Boolean*</span></span>

<span data-ttu-id="d3068-114">Ein *boolescher* Wert, der angibt, ob dem ausgeschriebenen Text ein Währungsname hinzugefügt werden muss.</span><span class="sxs-lookup"><span data-stu-id="d3068-114">A *Boolean* value that indicates whether a currency name must be added to the spelled-out text.</span></span>

<span data-ttu-id="d3068-115">`decimal points`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="d3068-115">`decimal points`: *Integer*</span></span>

<span data-ttu-id="d3068-116">Der Wert *Integer*, der die Anzahl der Dezimalstellen angibt, die der ausgeschriebene Text haben sollte.</span><span class="sxs-lookup"><span data-stu-id="d3068-116">An *Integer* value that indicates the number of decimal places that the spelled-out text should have.</span></span>

## <a name="return-values"></a><span data-ttu-id="d3068-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d3068-117">Return values</span></span>

<span data-ttu-id="d3068-118">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="d3068-118">*String*</span></span>

<span data-ttu-id="d3068-119">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="d3068-119">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d3068-120">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="d3068-120">Usage notes</span></span>

<span data-ttu-id="d3068-121">Der Sprachcode ist optional.</span><span class="sxs-lookup"><span data-stu-id="d3068-121">The language code is optional.</span></span> <span data-ttu-id="d3068-122">Wenn er als leere Zeichenfolge definiert ist, wird stattdessen der Sprachcode für den ausgeführten Kontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3068-122">If it's defined as an empty string, the language code for the running context is used.</span></span> <span data-ttu-id="d3068-123">Der Standard-Sprachcode lautet **EN-US**.</span><span class="sxs-lookup"><span data-stu-id="d3068-123">The default language code is **EN-US**.</span></span> <span data-ttu-id="d3068-124">Der Sprachcode für den laufenden Kontext ist im Element **Ordner** oder **Datei** des Formats der elektronischen Berichterstellung (EB) definiert, das ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3068-124">The language code for the running context is defined in a **Folder** or **File** element of the Electronic reporting (ER) format that is running.</span></span>

<span data-ttu-id="d3068-125">Der Währungscode ist optional.</span><span class="sxs-lookup"><span data-stu-id="d3068-125">The currency code is optional.</span></span> <span data-ttu-id="d3068-126">Wenn er als leere Zeichenfolge definiert ist, wird stattdessen die Unternehmenswährung für den ausgeführten Kontext verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3068-126">If it's defined as an empty string, the company currency for the running context is used.</span></span>

> [!NOTE] 
> <span data-ttu-id="d3068-127">Die Argumente `print currency name flag` und `decimal points` werden nur für die folgenden Sprachcodes analysiert: **CS**, **ET**, **HU**, **LT**, **LV**, **PL** und **RU**.</span><span class="sxs-lookup"><span data-stu-id="d3068-127">The `print currency name flag` and `decimal points` arguments are analyzed only for the following language codes: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**.</span></span> <span data-ttu-id="d3068-128">Darüber hinaus wird das Argument `print currency name flag` nur für Unternehmen analysiert, bei denen der Landes- oder Regionskontext die Deklination von Währungsnamen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d3068-128">Additionally, the `print currency name flag` argument is analyzed only for companies where the country's or region's context supports declension of currency names.</span></span>

## <a name="example-1"></a><span data-ttu-id="d3068-129">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3068-129">Example 1</span></span>

<span data-ttu-id="d3068-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` gibt **"One Thousand Two Hundred Thirty Four and 56"** zurück.</span><span class="sxs-lookup"><span data-stu-id="d3068-130">`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returns **"One Thousand Two Hundred Thirty Four and 56"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="d3068-131">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d3068-131">Example 2</span></span>

<span data-ttu-id="d3068-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` gibt **"Sto dwadzieścia"** zurück.</span><span class="sxs-lookup"><span data-stu-id="d3068-132">`NUMERALSTOTEXT (120, "PL", "", false, 0)` returns **"Sto dwadzieścia"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="d3068-133">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d3068-133">Example 3</span></span>

<span data-ttu-id="d3068-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` gibt **"Сто двадцать евро 21 евроцент"** zurück.</span><span class="sxs-lookup"><span data-stu-id="d3068-134">`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returns **"Сто двадцать евро 21 евроцент"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d3068-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3068-135">Additional resources</span></span>

[<span data-ttu-id="d3068-136">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="d3068-136">Text functions</span></span>](er-functions-category-text.md)
