---
title: MID EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der MID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: e2addace5c5606ebaae56ca658700347978a805b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744718"
---
# <a name="mid-er-function"></a><span data-ttu-id="d13a4-103">MID EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="d13a4-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d13a4-104">Die Funktion `MID` gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab der angegebenen Zeichenfolge angibt, wobei an der angegebenen Position gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d13a4-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="d13a4-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d13a4-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="d13a4-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="d13a4-106">Arguments</span></span>

<span data-ttu-id="d13a4-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="d13a4-107">`text`: *String*</span></span>

<span data-ttu-id="d13a4-108">Der Wert *String*, der den Text angibt, von dem Zeichen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d13a4-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="d13a4-109">`starting position`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="d13a4-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="d13a4-110">Der Wert *Integer*, der die Position des ersten Zeichens angibt, das aus dem angegebenen Text zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="d13a4-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="d13a4-111">`number of characters`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="d13a4-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="d13a4-112">Der Wert *Integer*, der die Anzahl der Zeichen angibt, die von der angegebenen Startposition aus zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d13a4-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="d13a4-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d13a4-113">Return values</span></span>

<span data-ttu-id="d13a4-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="d13a4-114">*String*</span></span>

<span data-ttu-id="d13a4-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="d13a4-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d13a4-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="d13a4-116">Usage notes</span></span>

<span data-ttu-id="d13a4-117">Wenn der Wert des Arguments `starting position` weniger als 0 (null) beträgt, werden die Zeichen, die zurückgegeben werden, ab der ersten Position in der angegebenen Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d13a4-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="d13a4-118">Wenn der Wert des Arguments `starting position` die Länge der angegebenen Zeichenfolge überschreitet, wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d13a4-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="d13a4-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="d13a4-119">Example</span></span>

<span data-ttu-id="d13a4-120">`MID ("Sample", 2, 3)` gibt **"amp"** zurück.</span><span class="sxs-lookup"><span data-stu-id="d13a4-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d13a4-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d13a4-121">Additional resources</span></span>

[<span data-ttu-id="d13a4-122">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="d13a4-122">Text functions</span></span>](er-functions-category-text.md)
