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
ms.openlocfilehash: 5903f562b5f266572f999756539fa7b9ef145023
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041330"
---
# <span data-ttu-id="ec804-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="ec804-103"><a name="ROUNDAMOUNT">ROUNDAMOUNT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec804-104">Die Funktion `ROUNDAMOUNT` gibt den Wert *Real* zurück, der das Ergebnis der Rundung des angegebenen Betrags auf das nächste Vielfache der angegebenen Anzahl gemäß der angegebenen Rundungsregel darstellt.</span><span class="sxs-lookup"><span data-stu-id="ec804-104">The `ROUNDAMOUNT` function returns a *Real* value as the result of the rounding of the specified number to the nearest multiple of another number according to the specified rounding rule.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec804-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec804-105">Syntax</span></span>

```vb
ROUNDAMOUNT (number, decimals, round rule)
```

## <a name="arguments"></a><span data-ttu-id="ec804-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="ec804-106">Arguments</span></span>

<span data-ttu-id="ec804-107">`number`: *Int* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="ec804-107">`number`: *Int* or *Real*</span></span>

<span data-ttu-id="ec804-108">Ein numerischer Wert, der gerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ec804-108">A numeric value that must be rounded.</span></span>

<span data-ttu-id="ec804-109">`decimals`: *Int* oder *Real*</span><span class="sxs-lookup"><span data-stu-id="ec804-109">`decimals`: *Int* or *Real*</span></span>

<span data-ttu-id="ec804-110">Die Zahl, die der Wert des Parameters `number` auf ein Vielfaches gerundet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ec804-110">The number that the value of the `number` parameter must be rounded to a multiple of.</span></span>

<span data-ttu-id="ec804-111">`round rule`: *Enum value*</span><span class="sxs-lookup"><span data-stu-id="ec804-111">`round rule`: *Enum value*</span></span>

<span data-ttu-id="ec804-112">Ein Aufzählungswert der Aufzählung **RoundOffType**, die die Rundungsregel definiert.</span><span class="sxs-lookup"><span data-stu-id="ec804-112">An enumeration value of the **RoundOffType** enumeration that defines the rounding rule.</span></span> <span data-ttu-id="ec804-113">Diese Aufzählung bietet die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="ec804-113">This enumeration offers the following values:</span></span>

- <span data-ttu-id="ec804-114">Normal (gewöhnlich)</span><span class="sxs-lookup"><span data-stu-id="ec804-114">Normal (Ordinary)</span></span>
- <span data-ttu-id="ec804-115">Abrunden (RoundDown)</span><span class="sxs-lookup"><span data-stu-id="ec804-115">Downward (RoundDown)</span></span>
- <span data-ttu-id="ec804-116">Aufrunden (RoundUp)</span><span class="sxs-lookup"><span data-stu-id="ec804-116">Rounding-up (RoundUp)</span></span>

## <a name="return-values"></a><span data-ttu-id="ec804-117">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ec804-117">Return values</span></span>

<span data-ttu-id="ec804-118">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="ec804-118">*Real*</span></span>

<span data-ttu-id="ec804-119">Der sich ergebende numerische Wert ist ein Vielfaches des Wertes, der durch den Parameter `decimals` angegeben wird, und kommt dem durch den Parameter `number` angegebenen Wert am nächsten.</span><span class="sxs-lookup"><span data-stu-id="ec804-119">The resulting numeric value is a multiple of the value specified by the `decimals` parameter and is closest to the value specified by the `number` parameter.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec804-120">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="ec804-120">Usage notes</span></span>

<span data-ttu-id="ec804-121">Wenn der Parameter `number` Null ist, gibt diese Funktion immer Null zurück.</span><span class="sxs-lookup"><span data-stu-id="ec804-121">When the `number` parameter is zero, this function always returns zero.</span></span>

<span data-ttu-id="ec804-122">Wenn der Parameter `decimals` Null ist, rundet diese Funktion auf den Standardrundungswert.</span><span class="sxs-lookup"><span data-stu-id="ec804-122">When the `decimals` parameter is zero, this function rounds to the default round-off value.</span></span> <span data-ttu-id="ec804-123">Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, beträgt der Standardrundungswert **0,01**.</span><span class="sxs-lookup"><span data-stu-id="ec804-123">When the `round rule` parameter is set to **RoundOffType.Ordinary**, the default round-off value is **0.01**.</span></span> <span data-ttu-id="ec804-124">Andernfalls beträgt der Standardrundungswert **1,0**.</span><span class="sxs-lookup"><span data-stu-id="ec804-124">Otherwise, the default round-off value is **1.0**.</span></span>

<span data-ttu-id="ec804-125">Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, rundet diese Funktion auf den nächsten Rundungsbetrag.</span><span class="sxs-lookup"><span data-stu-id="ec804-125">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function rounds to the nearest round-off amount.</span></span>

<span data-ttu-id="ec804-126">Wenn der Parameter `round rule` auf **RoundOffType.RoundDown** festgelegt ist, rundet diese Funktion in Richtung Null auf den nächsten Rundungsbetrag.</span><span class="sxs-lookup"><span data-stu-id="ec804-126">When the `round rule` parameter is set to **RoundOffType.RoundDown**, this function rounds towards zero to the nearest round-off amount.</span></span>

<span data-ttu-id="ec804-127">Wenn der Parameter `round rule` auf **RoundOffType.RoundUp** festgelegt ist, rundet diese Funktion weg von Null auf den nächsten Rundungsbetrag.</span><span class="sxs-lookup"><span data-stu-id="ec804-127">When the `round rule` parameter is set to **RoundOffType.RoundUp**, this function rounds away from zero to the nearest round-off amount.</span></span>

<span data-ttu-id="ec804-128">Wenn der Parameter `round rule` auf **RoundOffType.Ordinary** festgelegt ist, verhält sich diese Funktion wie die [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel-Funktion und die [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ Funktion.</span><span class="sxs-lookup"><span data-stu-id="ec804-128">When the `round rule` parameter is set to **RoundOffType.Ordinary**, this function behaves like the [MROUND](https://support.office.com/article/mround-function-c299c3b0-15a5-426d-aa4b-d2d5b3baf427) Excel function and the [ROUND](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-ref/xpp-math-run-time-functions#round) X++ function.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec804-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ec804-129">Remarks</span></span>

<span data-ttu-id="ec804-130">Um einen numerischen Wert auf eine bestimmte Anzahl von Dezimalstellen zu runden, verwenden Sie die Funktion [ROUND](er-functions-mathematical-round.md).</span><span class="sxs-lookup"><span data-stu-id="ec804-130">To round a numeric value to a specified number of decimal places, use the [ROUND](er-functions-mathematical-round.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="ec804-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ec804-131">Example</span></span>

<span data-ttu-id="ec804-132">Wenn der Parameter **model.RoundOff** auf **RoundOffType.Ordinary** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 zurück.</span><span class="sxs-lookup"><span data-stu-id="ec804-132">If the **model.RoundOff** parameter is set to **RoundOffType.Ordinary**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="ec804-133">Wenn der Parameter **model.RoundOff** auf **RoundOffType.RoundDown** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 7,35 zurück.</span><span class="sxs-lookup"><span data-stu-id="ec804-133">If the **model.RoundOff** parameter is set to **RoundOffType.RoundDown**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 7.35.</span></span> 

<span data-ttu-id="ec804-134">Wenn der Parameter **model.RoundOff** auf **RoundOffType.RoundUp** festgelegt ist, gibt `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` 8,4 zurück.</span><span class="sxs-lookup"><span data-stu-id="ec804-134">If the **model.RoundOff** parameter is set to **RoundOffType.RoundUp**, `ROUNDAMOUNT (7.45, 1.05, model.RoundOff)` returns 8.4.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec804-135">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ec804-135">Additional resources</span></span>

[<span data-ttu-id="ec804-136">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="ec804-136">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)

[<span data-ttu-id="ec804-137">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="ec804-137">Mathematical functions</span></span>](er-functions-category-mathematical.md)
