---
title: ROUNDDOWN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUNDDOWN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 89fc134ec11a47506211ce68ec3aaf966d9a308b
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744462"
---
# <a name="rounddown-er-function"></a><span data-ttu-id="c5f27-103">ROUNDDOWN EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="c5f27-103">ROUNDDOWN ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5f27-104">Die Funktion `ROUNDDOWN` gibt die angegebene Zahl mit dem Wert *Real* zurück, nachdem sie auf die angegebene Zahl der Dezimalstellen abgerundet wurde.</span><span class="sxs-lookup"><span data-stu-id="c5f27-104">The `ROUNDDOWN` function returns the specified number as a *Real* value after it has been rounded down to the specified number of decimal places.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5f27-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5f27-105">Syntax</span></span>

```vb
ROUNDDOWN (number, decimals)
```

## <a name="arguments"></a><span data-ttu-id="c5f27-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="c5f27-106">Arguments</span></span>

<span data-ttu-id="c5f27-107">`number`: *Real*</span><span class="sxs-lookup"><span data-stu-id="c5f27-107">`number`: *Real*</span></span>

<span data-ttu-id="c5f27-108">Ein numerischer Wert, der abgerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c5f27-108">A numeric value that must be rounded down.</span></span>

<span data-ttu-id="c5f27-109">`decimals`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="c5f27-109">`decimals`: *Integer*</span></span>

<span data-ttu-id="c5f27-110">Ein numerischer Wert, der die Anzahl der Dezimalstellen angibt.</span><span class="sxs-lookup"><span data-stu-id="c5f27-110">A numeric value that represents the number of decimal places.</span></span>

## <a name="return-values"></a><span data-ttu-id="c5f27-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c5f27-111">Return values</span></span>

<span data-ttu-id="c5f27-112">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="c5f27-112">*Real*</span></span>

<span data-ttu-id="c5f27-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="c5f27-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c5f27-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="c5f27-114">Usage notes</span></span>

<span data-ttu-id="c5f27-115">Diese Funktion verhält sich wie [RUNDUNG](er-functions-mathematical-round.md), rundet die angegebene Zahl aber immer ab (in Richtung null).</span><span class="sxs-lookup"><span data-stu-id="c5f27-115">This function behaves like [ROUND](er-functions-mathematical-round.md), but it always rounds the specified number down (toward zero).</span></span>

## <a name="example-1"></a><span data-ttu-id="c5f27-116">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c5f27-116">Example 1</span></span>

<span data-ttu-id="c5f27-117">`ROUNDDOWN (1200.767, 2)` rundet auf bis zu zwei Dezimalstellen ab und gibt den Wert **1200.76** zurück.</span><span class="sxs-lookup"><span data-stu-id="c5f27-117">`ROUNDDOWN (1200.767, 2)` rounds down to two decimal places and returns **1200.76**.</span></span> 

## <a name="example-2"></a><span data-ttu-id="c5f27-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="c5f27-118">Example 2</span></span>

<span data-ttu-id="c5f27-119">`ROUNDDOWN (1700.767, -3)` rundet auf das nächste Vielfache von 1.000 ab und gibt den Wert **1000** zurück.</span><span class="sxs-lookup"><span data-stu-id="c5f27-119">`ROUNDDOWN (1700.767, -3)` rounds down to the nearest multiple of 1,000 and returns **1000**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5f27-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c5f27-120">Additional resources</span></span>

[<span data-ttu-id="c5f27-121">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="c5f27-121">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]