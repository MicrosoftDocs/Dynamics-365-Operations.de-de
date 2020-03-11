---
title: ROUNDDOWN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUNDDOWN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 92150bb23e76f82907e0f3e8f0738b25801958bf
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041560"
---
# <span data-ttu-id="e2467-103"><a name="ROUNDDOWN">ROUNDDOWN EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="e2467-103"><a name="ROUNDDOWN">ROUNDDOWN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2467-104">Die Funktion `ROUNDDOWN` gibt die angegebene Zahl mit dem Wert *Real* zurück, nachdem sie auf die angegebene Zahl der Dezimalstellen abgerundet wurde.</span><span class="sxs-lookup"><span data-stu-id="e2467-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2467-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2467-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="e2467-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="e2467-106">Arguments</span></span>

<span data-ttu-id="e2467-107">`number`: *Real*</span><span class="sxs-lookup"><span data-stu-id="e2467-107">`number`: *Real*</span></span>

<span data-ttu-id="e2467-108">Ein numerischer Wert, der abgerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="e2467-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="e2467-109">`decimals`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="e2467-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="e2467-110">Ein numerischer Wert, der die Anzahl der Dezimalstellen angibt.</span><span class="sxs-lookup"><span data-stu-id="e2467-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="e2467-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e2467-111">Return values</span></span>

<span data-ttu-id="e2467-112">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="e2467-112">*Real*</span></span>

<span data-ttu-id="e2467-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="e2467-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e2467-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="e2467-114">Usage notes</span></span>

<span data-ttu-id="e2467-115">Diese Funktion verhält sich wie [RUNDUNG](er-functions-mathematical-round.md), rundet die angegebene Zahl aber immer ab (in Richtung null).</span><span class="sxs-lookup"><span data-stu-id="e2467-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="e2467-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e2467-116">Example 1</span></span>

<span data-ttu-id="e2467-117">`ROUNDDOWN (1200.767, 2)` rundet auf bis zu zwei Dezimalstellen ab und gibt den Wert **1200.76** zurück.</span><span class="sxs-lookup"><span data-stu-id="e2467-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="e2467-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e2467-118">Example 2</span></span>

<span data-ttu-id="e2467-119">`ROUNDDOWN (1700.767, -3)` rundet auf das nächste Vielfache von 1.000 ab und gibt den Wert **1000** zurück.</span><span class="sxs-lookup"><span data-stu-id="e2467-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2467-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2467-120">Additional resources</span></span>

[<span data-ttu-id="e2467-121">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="e2467-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)
