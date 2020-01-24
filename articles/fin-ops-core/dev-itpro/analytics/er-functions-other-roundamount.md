---
title: ROUNDAMOUNT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ROUNDAMOUNT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: c68933352da1f9c7dc5dad76e8635981f8a89fce
ms.sourcegitcommit: 9291e6dc0de076a16684980e528c5aa98845bb34
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2918978"
---
# <span data-ttu-id="c5bd2-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="c5bd2-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c5bd2-104">Die Funktion `ROUNDAMOUNT` gibt den Wert *Real* zurück, der das Ergebnis der Rundung des angegebenen Betrags auf das nächste Vielfache der angegebenen Anzahl gemäß der angegebenen Rundungsregel darstellt.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5bd2-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c5bd2-105">Syntax</span></span>

```
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="c5bd2-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="c5bd2-106">Arguments</span></span>

<span data-ttu-id="c5bd2-107">`number`: *Int* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="c5bd2-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="c5bd2-108">Ein numerischer Wert, der gerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="c5bd2-109">`decimals`: *Int* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="c5bd2-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="c5bd2-110">Die Zahl, die der Wert des Parameters `number` auf ein Vielfaches gerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="c5bd2-111">`round rule`: *Enum value*</span><span class="sxs-lookup"><span data-stu-id="c5bd2-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="c5bd2-112">Ein Aufzählungswert der Aufzählung **RoundOffType**, die die Rundungsregel definiert.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="c5bd2-113">Diese Aufzählung bietet die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="c5bd2-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="c5bd2-114">Normal (gewöhnlich)</span><span class="sxs-lookup"><span data-stu-id="c5bd2-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="c5bd2-115">Abrunden (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="c5bd2-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="c5bd2-116">Aufrunden (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="c5bd2-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="c5bd2-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c5bd2-117">Return values</span></span>

<span data-ttu-id="c5bd2-118">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="c5bd2-118">*Real*</span></span>

<span data-ttu-id="c5bd2-119">Der sich ergebende numerische Wert ist ein Vielfaches des Wertes, der durch den Parameter `decimals` angegeben wird, und kommt dem durch den Parameter `number` angegebenen Wert am nächsten.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c5bd2-120">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="c5bd2-120">Usage notes</span></span>

<span data-ttu-id="c5bd2-121">Wenn der Parameter `number` Null ist, gibt diese Funktion immer Null zurück.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="c5bd2-122">Wenn der Parameter `decimals` Null ist, rundet diese Funktion auf den Standardrundungswert.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="c5bd2-123">Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, beträgt der Standardrundungswert **0,01**.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="c5bd2-124">Andernfalls beträgt der Standardrundungswert **1,0**.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="c5bd2-125">Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, rundet diese Funktion auf den nächsten Rundungsbetrag.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="c5bd2-126">Wenn der Parameter `round rule` auf **RoundOffType.RoundDown** festgelegt ist, rundet diese Funktion in Richtung Null auf den nächsten Rundungsbetrag.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="c5bd2-127">Wenn der Parameter `round rule` auf **RoundOffType.RoundUp** festgelegt ist, rundet diese Funktion weg von Null auf den nächsten Rundungsbetrag.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="c5bd2-128">Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, verhält sich diese Funktion wie die [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-Funktion und die [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ Funktion.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5bd2-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5bd2-129">Remarks</span></span>

<span data-ttu-id="c5bd2-130">Um einen numerischen Wert auf eine bestimmte Anzahl von Dezimalstellen zu runden, verwenden Sie die Funktion [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="c5bd2-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="c5bd2-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c5bd2-131">Example</span></span>

<span data-ttu-id="c5bd2-132">Wenn der Parameter **model.RoundOff** auf **RoundOffType.Ordinary** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 zurück.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="c5bd2-133">Wenn der Parameter **model.RoundOff** auf **RoundOffType.RoundDown** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 zurück.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="c5bd2-134">Wenn der Parameter **model.RoundOff** auf **RoundOffType.RoundUp** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4 zurück.</span><span class="sxs-lookup"><span data-stu-id="c5bd2-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c5bd2-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c5bd2-135">Additional resources</span></span>

[<span data-ttu-id="c5bd2-136">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="c5bd2-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="c5bd2-137">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="c5bd2-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
