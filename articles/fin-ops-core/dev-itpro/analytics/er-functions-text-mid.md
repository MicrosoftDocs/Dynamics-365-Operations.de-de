---
title: MID EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der MID-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: e0520bc54465f00d36e88787933b291847dee852
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562732"
---
# <a name="mid-er-function"></a><span data-ttu-id="2aabf-103">MID EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="2aabf-103">MID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2aabf-104">Die Funktion `MID` gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab der angegebenen Zeichenfolge angibt, wobei an der angegebenen Position gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="2aabf-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="2aabf-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2aabf-105">Syntax</span></span>

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="2aabf-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="2aabf-106">Arguments</span></span>

<span data-ttu-id="2aabf-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="2aabf-107">`text`: *String*</span></span>

<span data-ttu-id="2aabf-108">Der Wert *String*, der den Text angibt, von dem Zeichen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2aabf-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="2aabf-109">`starting position`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="2aabf-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="2aabf-110">Der Wert *Integer*, der die Position des ersten Zeichens angibt, das aus dem angegebenen Text zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="2aabf-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="2aabf-111">`number of characters`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="2aabf-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="2aabf-112">Der Wert *Integer*, der die Anzahl der Zeichen angibt, die von der angegebenen Startposition aus zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2aabf-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="2aabf-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="2aabf-113">Return values</span></span>

<span data-ttu-id="2aabf-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="2aabf-114">*String*</span></span>

<span data-ttu-id="2aabf-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="2aabf-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2aabf-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="2aabf-116">Usage notes</span></span>

<span data-ttu-id="2aabf-117">Wenn der Wert des Arguments `starting position` weniger als 0 (null) beträgt, werden die Zeichen, die zurückgegeben werden, ab der ersten Position in der angegebenen Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2aabf-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="2aabf-118">Wenn der Wert des Arguments `starting position` die Länge der angegebenen Zeichenfolge überschreitet, wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2aabf-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="2aabf-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="2aabf-119">Example</span></span>

<span data-ttu-id="2aabf-120">`MID ("Sample", 2, 3)` gibt **"amp"** zurück.</span><span class="sxs-lookup"><span data-stu-id="2aabf-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2aabf-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2aabf-121">Additional resources</span></span>

[<span data-ttu-id="2aabf-122">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="2aabf-122">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]