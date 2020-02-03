---
title: OR EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der OR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 81a596f5206b23001feea553adcdf6c904572775
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917119"
---
# <span data-ttu-id="1fe17-103"><a name="OR">OR EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="1fe17-103"><a name="OR">OR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fe17-104">Die Funktion `OR` gibt den *booleschen* Wert **FALSE** zurück, wenn alle angegebenen Bedingungen falsch sind.</span><span class="sxs-lookup"><span data-stu-id="1fe17-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="1fe17-105">Wenn eine der angegebenen Bedingungen wahr ist, gibt die Funktion den *booleschen* Wert **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="1fe17-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fe17-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fe17-106">Syntax</span></span>

```
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="1fe17-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="1fe17-107">Arguments</span></span>

<span data-ttu-id="1fe17-108">`condition 1`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="1fe17-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="1fe17-109">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="1fe17-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="1fe17-110">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1fe17-110">This argument is required.</span></span>

<span data-ttu-id="1fe17-111">`condition N`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="1fe17-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="1fe17-112">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="1fe17-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="1fe17-113">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="1fe17-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="1fe17-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1fe17-114">Return values</span></span>

<span data-ttu-id="1fe17-115">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="1fe17-115">*Boolean*</span></span>

<span data-ttu-id="1fe17-116">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="1fe17-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="1fe17-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1fe17-117">Example</span></span>

<span data-ttu-id="1fe17-118">`OR (1=2, "a"="a")` gibt **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="1fe17-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1fe17-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1fe17-119">Additional resources</span></span>

[<span data-ttu-id="1fe17-120">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="1fe17-120">Logical functions</span></span>](er-functions-category-logical.md)