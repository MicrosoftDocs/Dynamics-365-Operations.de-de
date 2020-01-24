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
ms.openlocfilehash: e178b01740954b46e2afbd2a2be6200a652a18c0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915601"
---
# <span data-ttu-id="7a4c5-103"><a name="MID">MID EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="7a4c5-103"><a name="MID">MID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7a4c5-104">Die Funktion `MID` gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab der angegebenen Zeichenfolge angibt, wobei an der angegebenen Position gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-104">The `MID` function returns a *String* value that presents the specified number of characters from the specified string, starting at the specified position.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a4c5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a4c5-105">Syntax</span></span>

```
MID (text, starting position, number of characters)
```

## <a name="arguments"></a><span data-ttu-id="7a4c5-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="7a4c5-106">Arguments</span></span>

<span data-ttu-id="7a4c5-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="7a4c5-107">`text`: *String*</span></span>

<span data-ttu-id="7a4c5-108">Der Wert *String*, der den Text angibt, von dem Zeichen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-108">A *String* value that specifies the text to return characters from.</span></span>

<span data-ttu-id="7a4c5-109">`starting position`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="7a4c5-109">`starting position`: *Integer*</span></span>

<span data-ttu-id="7a4c5-110">Der Wert *Integer*, der die Position des ersten Zeichens angibt, das aus dem angegebenen Text zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-110">An *Integer* value that specifies the position of the first character that must be returned from the specified text.</span></span>

<span data-ttu-id="7a4c5-111">`number of characters`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="7a4c5-111">`number of characters`: *Integer*</span></span>

<span data-ttu-id="7a4c5-112">Der Wert *Integer*, der die Anzahl der Zeichen angibt, die von der angegebenen Startposition aus zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-112">An *Integer* value that specifies the number of characters that must be returned, starting at the specified starting position.</span></span>

## <a name="return-values"></a><span data-ttu-id="7a4c5-113">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="7a4c5-113">Return values</span></span>

<span data-ttu-id="7a4c5-114">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="7a4c5-114">*String*</span></span>

<span data-ttu-id="7a4c5-115">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-115">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="7a4c5-116">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="7a4c5-116">Usage notes</span></span>

<span data-ttu-id="7a4c5-117">Wenn der Wert des Arguments `starting position` weniger als 0 (null) beträgt, werden die Zeichen, die zurückgegeben werden, ab der ersten Position in der angegebenen Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-117">If the value of the `starting position` argument is less than 0 (zero), the characters that are returned are counted from the first position in the specified string.</span></span>

<span data-ttu-id="7a4c5-118">Wenn der Wert des Arguments `starting position` die Länge der angegebenen Zeichenfolge überschreitet, wird eine leere Zeichenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-118">If the value of the `starting position` argument exceeds length of the specified string, an empty string is returned.</span></span>

## <a name="example"></a><span data-ttu-id="7a4c5-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="7a4c5-119">Example</span></span>

<span data-ttu-id="7a4c5-120">`MID ("Sample", 2, 3)` gibt **"amp"** zurück.</span><span class="sxs-lookup"><span data-stu-id="7a4c5-120">`MID ("Sample", 2, 3)` returns **"amp"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7a4c5-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="7a4c5-121">Additional resources</span></span>

[<span data-ttu-id="7a4c5-122">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="7a4c5-122">Text functions</span></span>](er-functions-category-text.md)
