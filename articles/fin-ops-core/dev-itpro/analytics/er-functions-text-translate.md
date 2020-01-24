---
title: TRANSLATE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von TRANSLATE bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11954f3e48d8dc2257b3a0bc8768df47af3c5c0c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916705"
---
# <span data-ttu-id="de77f-103"><a name="TRANSLATE">TRANSLATE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="de77f-103"><a name="TRANSLATE">TRANSLATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="de77f-104">Die Funktion `TRANSLATE` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er ganz oder teilweise durch eine andere Zeichenfolge ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="de77f-104">The `TRANSLATE` function returns the specified text string as a *String* value after all or part of it has been replaced with another string.</span></span>

## <a name="syntax"></a><span data-ttu-id="de77f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="de77f-105">Syntax</span></span>

```
TRANSLATE (text , pattern, replacement)
```

## <a name="arguments"></a><span data-ttu-id="de77f-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="de77f-106">Arguments</span></span>

<span data-ttu-id="de77f-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="de77f-107">`text`: *String*</span></span>

<span data-ttu-id="de77f-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="de77f-108">The valid path of a data source of the *String* type.</span></span>

<span data-ttu-id="de77f-109">`pattern`: *String*</span><span class="sxs-lookup"><span data-stu-id="de77f-109">`pattern`: *String*</span></span>

<span data-ttu-id="de77f-110">Der Text, der ersetzt werden muss.</span><span class="sxs-lookup"><span data-stu-id="de77f-110">The text that must be replaced.</span></span>

<span data-ttu-id="de77f-111">`replacement`: *String*</span><span class="sxs-lookup"><span data-stu-id="de77f-111">`replacement`: *String*</span></span>

<span data-ttu-id="de77f-112">Den als Ersatz zu verwendenden Text.</span><span class="sxs-lookup"><span data-stu-id="de77f-112">The text to use as a replacement.</span></span>

## <a name="return-values"></a><span data-ttu-id="de77f-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="de77f-113">Return values</span></span>

<span data-ttu-id="de77f-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="de77f-114">*String*</span></span>

<span data-ttu-id="de77f-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="de77f-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="de77f-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="de77f-116">Example</span></span>

<span data-ttu-id="de77f-117">`TRANSLATE ("abcdef", "cd", "GH")` ersetzt das Muster **"cd"** durch die Zeichenfolge **"GH"** und gibt **"abGHef"** zurück.</span><span class="sxs-lookup"><span data-stu-id="de77f-117">`TRANSLATE ("abcdef", "cd", "GH")` replaces the pattern **"cd"** with the string **"GH"** and returns **"abGHef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="de77f-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="de77f-118">Additional resources</span></span>

[<span data-ttu-id="de77f-119">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="de77f-119">Text functions</span></span>](er-functions-category-text.md)
