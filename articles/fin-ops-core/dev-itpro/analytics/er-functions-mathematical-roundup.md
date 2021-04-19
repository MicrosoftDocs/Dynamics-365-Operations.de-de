---
title: ROUNDUP EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUNDUP-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 4898f596108ff3c563da55a567a10da987d62d33
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744438"
---
# <a name="roundup-er-function"></a><span data-ttu-id="5b19b-103">ROUNDUP EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="5b19b-103">ROUNDUP ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b19b-104">Die Funktion `ROUNDUP` gibt die angegebene Zahl mit dem Wert *Real* zurück, nachdem sie auf die angegebene Zahl der Dezimalstellen aufgerundet wurde.</span><span class="sxs-lookup"><span data-stu-id="5b19b-104">The `ROUNDUP` function returns the specified number as a *Real* value after it has been rounded up to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b19b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5b19b-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="5b19b-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="5b19b-106">Arguments</span></span>

<span data-ttu-id="5b19b-107">`number`: *Real*</span><span class="sxs-lookup"><span data-stu-id="5b19b-107">`number`: *Real*</span></span>

<span data-ttu-id="5b19b-108">Ein numerischer Wert, der aufgerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="5b19b-108">A numeric value that must be rounded up.</span></span>

<span data-ttu-id="5b19b-109">`decimals`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="5b19b-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="5b19b-110">Ein numerischer Wert, der die Anzahl der Dezimalstellen angibt.</span><span class="sxs-lookup"><span data-stu-id="5b19b-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="5b19b-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5b19b-111">Return values</span></span>

<span data-ttu-id="5b19b-112">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="5b19b-112">*Real*</span></span>

<span data-ttu-id="5b19b-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="5b19b-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5b19b-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="5b19b-114">Usage notes</span></span>

<span data-ttu-id="5b19b-115">Diese Funktion verhält sich wie [RUNDUNG](er-functions-mathematical-round.md), rundet die angegebene Zahl aber immer auf (weg von null).</span><span class="sxs-lookup"><span data-stu-id="5b19b-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number up (away from zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="5b19b-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5b19b-116">Example 1</span></span>

<span data-ttu-id="5b19b-117">`ROUNDUP (1200.763, 2)` rundet auf bis zu zwei Dezimalstellen und gibt den Wert **1200.77** zurück.</span><span class="sxs-lookup"><span data-stu-id="5b19b-117">`ROUNDUP (1200.763, 2)` rounds up to two decimal places and returns **1200.77**.</span></span>

## <a name="example-2"></a><span data-ttu-id="5b19b-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5b19b-118">Example 2</span></span>

<span data-ttu-id="5b19b-119">`ROUNDUP (1200.767, -3)` rundet auf das nächste Vielfache von 1.000 auf und gibt den Wert **2000** zurück.</span><span class="sxs-lookup"><span data-stu-id="5b19b-119">`ROUNDUP (1200.767, -3)` rounds up to the nearest multiple of 1,000 and returns **2000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5b19b-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5b19b-120">Additional resources</span></span>

[<span data-ttu-id="5b19b-121">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="5b19b-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]