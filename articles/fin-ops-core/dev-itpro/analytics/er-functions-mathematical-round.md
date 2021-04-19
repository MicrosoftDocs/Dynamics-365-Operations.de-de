---
title: ROUND EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUND-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 10/21/2020
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
ms.openlocfilehash: ce0f50cd5e544455626862e44b774dba39cf6e57
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744486"
---
# <a name="round-er-function"></a><span data-ttu-id="a8cea-103">ROUND EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="a8cea-103">ROUND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a8cea-104">Die Funktion `ROUND` gibt die angegebene Zahl mit dem Wert *Real* zurück, nachdem sie auf die angegebene Zahl der Dezimalstellen gerundet wurde.</span><span class="sxs-lookup"><span data-stu-id="a8cea-104">The `ROUND` function returns the specified number as a *Real* value after it has been rounded to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8cea-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8cea-105">Syntax</span></span>

```vb
ROUND (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="a8cea-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="a8cea-106">Arguments</span></span>

<span data-ttu-id="a8cea-107">`number`: *Real*</span><span class="sxs-lookup"><span data-stu-id="a8cea-107">`number`: *Real*</span></span>

<span data-ttu-id="a8cea-108">Ein numerischer Wert, der gerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="a8cea-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="a8cea-109">`decimals`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="a8cea-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="a8cea-110">Ein numerischer Wert, der die Anzahl der Dezimalstellen angibt.</span><span class="sxs-lookup"><span data-stu-id="a8cea-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="a8cea-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a8cea-111">Return values</span></span>

<span data-ttu-id="a8cea-112">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="a8cea-112">*Real*</span></span>

<span data-ttu-id="a8cea-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="a8cea-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="a8cea-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="a8cea-114">Usage notes</span></span>

<span data-ttu-id="a8cea-115">Wenn der Wert des Arguments `decimals` größer als 0 (null) ist, wird die angegebene Zahl auf genau so viele Dezimalstellen gerundet.</span><span class="sxs-lookup"><span data-stu-id="a8cea-115">If the value of the `decimals` argument is more than 0 (zero), the specified number is rounded to that many decimal places.</span></span>

<span data-ttu-id="a8cea-116">Wenn das Argument `decimals` den Wert **0** (null) hat, wird die angegebene Zahl auf die nächste gerade Ganzzahl gerundet.</span><span class="sxs-lookup"><span data-stu-id="a8cea-116">If the value of the `decimals` argument is **0** (zero), the specified number is rounded to the nearest even integer.</span></span>

<span data-ttu-id="a8cea-117">Wenn der Wert des Arguments `decimals` kleiner als 0 (null) ist, wir die angegebene Zahl links der Dezimalstelle gerundet.</span><span class="sxs-lookup"><span data-stu-id="a8cea-117">If the value of the `decimals` argument is less than 0 (zero), the specified number is rounded to the left of the decimal point.</span></span>

## <a name="example-1"></a><span data-ttu-id="a8cea-118">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a8cea-118">Example 1</span></span>

<span data-ttu-id="a8cea-119">`ROUND (1200.767, 2)` rundet auf zwei Dezimalstellen und gibt den Wert **1200.77** zurück.</span><span class="sxs-lookup"><span data-stu-id="a8cea-119">`ROUND (1200.767, 2)` rounds to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="a8cea-120">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a8cea-120">Example 2</span></span>

<span data-ttu-id="a8cea-121">`ROUND (1200.767, -3)` rundet auf das nächste Vielfache von 1.000 und gibt den Wert **1000** zurück.</span><span class="sxs-lookup"><span data-stu-id="a8cea-121">`ROUND (1200.767, -3)` rounds to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="example-3"></a><span data-ttu-id="a8cea-122">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a8cea-122">Example 3</span></span>

<span data-ttu-id="a8cea-123">`ROUND (1200.5, 0)` rundet auf die nächste gerade Ganzahl und gibt **1200** zurück, während `ROUND (1201.5, 0)` ebenfalls eine Rundung durchführt und **1202** zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="a8cea-123">`ROUND (1200.5, 0)` rounds to the nearest even integer and returns **1200**, while `ROUND (1201.5, 0)` does the same and returns **1202**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a8cea-124">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a8cea-124">Additional resources</span></span>

[<span data-ttu-id="a8cea-125">Mathematische Funktionen</span><span class="sxs-lookup"><span data-stu-id="a8cea-125">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]