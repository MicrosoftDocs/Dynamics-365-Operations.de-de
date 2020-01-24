---
title: ROUND EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUND-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c9384d5975e4a25d18ff741f87431daa4b0bbd7e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917073"
---
# <span data-ttu-id="aa403-103"><a name="ROUND">ROUND EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="aa403-103"><a name="ROUND">ROUND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa403-104">Die Funktion `ROUND` gibt die angegebene Zahl mit dem Wert *Real* zurück, nachdem sie auf die angegebene Zahl der Dezimalstellen gerundet wurde.</span><span class="sxs-lookup"><span data-stu-id="aa403-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa403-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa403-105">Syntax</span></span>

```
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="aa403-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="aa403-106">Arguments</span></span>

<span data-ttu-id="aa403-107">`number`: *Real*</span><span class="sxs-lookup"><span data-stu-id="aa403-107">`number`: *Real*</span></span>

<span data-ttu-id="aa403-108">Ein numerischer Wert, der gerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="aa403-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="aa403-109">`decimals`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="aa403-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="aa403-110">Ein numerischer Wert, der die Anzahl der Dezimalstellen angibt.</span><span class="sxs-lookup"><span data-stu-id="aa403-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="aa403-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="aa403-111">Return values</span></span>

<span data-ttu-id="aa403-112">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="aa403-112">*Real*</span></span>

<span data-ttu-id="aa403-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="aa403-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="aa403-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="aa403-114">Usage notes</span></span>

<span data-ttu-id="aa403-115">Wenn der Wert des Arguments `decimals` größer als 0 (null) ist, wird die angegebene Zahl auf genau so viele Dezimalstellen gerundet.</span><span class="sxs-lookup"><span data-stu-id="aa403-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="aa403-116">Wenn der Wert des Arguments `decimals` **0** (null) ist, wird die angegebene Zahl auf die nächste ganze Zahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="aa403-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest integer.</span></span>

<span data-ttu-id="aa403-117">Wenn der Wert des Arguments `decimals` kleiner als 0 (null) ist, wir die angegebene Zahl links der Dezimalstelle gerundet.</span><span class="sxs-lookup"><span data-stu-id="aa403-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="aa403-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="aa403-118">Example 1</span></span>

<span data-ttu-id="aa403-119">`ROUND (1200.767, 2)` rundet auf zwei Dezimalstellen und gibt den Wert **1200.77** zurück.</span><span class="sxs-lookup"><span data-stu-id="aa403-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="aa403-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="aa403-120">Example 2</span></span>

<span data-ttu-id="aa403-121">`ROUND (1200.767, -3)` rundet auf das nächste Vielfache von 1.000 und gibt den Wert **1000** zurück.</span><span class="sxs-lookup"><span data-stu-id="aa403-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa403-122">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aa403-122">Additional resources</span></span>

[<span data-ttu-id="aa403-123">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="aa403-123">Mathematical functions</span></span>](er-functions-category-mathematical.md)
