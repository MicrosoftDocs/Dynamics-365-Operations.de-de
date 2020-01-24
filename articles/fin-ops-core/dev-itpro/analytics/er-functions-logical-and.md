---
title: AND EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von AND bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: dd9c0ed0238009f70ad7a9bf5a5e19ebfb95cccc
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917165"
---
# <span data-ttu-id="14fbd-103"><a name="AND">AND EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="14fbd-103"><a name="AND">AND ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14fbd-104">Die Funktion `AND` gibt den *booleschen* Wert **TRUE** zurück, wenn alle angegebenen Bedingungen wahr sind.</span><span class="sxs-lookup"><span data-stu-id="14fbd-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="14fbd-105">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="14fbd-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="14fbd-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="14fbd-106">Syntax</span></span>

```
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="14fbd-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="14fbd-107">Arguments</span></span>

<span data-ttu-id="14fbd-108">`condition 1`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="14fbd-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="14fbd-109">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="14fbd-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="14fbd-110">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="14fbd-110">This argument is required.</span></span>

<span data-ttu-id="14fbd-111">`condition N`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="14fbd-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="14fbd-112">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="14fbd-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="14fbd-113">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="14fbd-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="14fbd-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="14fbd-114">Return values</span></span>

<span data-ttu-id="14fbd-115">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="14fbd-115">*Boolean*</span></span>

<span data-ttu-id="14fbd-116">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="14fbd-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="14fbd-117">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="14fbd-117">Usage notes</span></span>

<span data-ttu-id="14fbd-118">In den Argumenten logischer Funktionen können Sie Datenquellenverweise, numerische und Textwerte, Boolesche Werte, Vergleichsoperatoren und andere Funktionen für die elektronische Berichterstellung (EB) verwenden.</span><span class="sxs-lookup"><span data-stu-id="14fbd-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="14fbd-119">Alle Argumente müssen jedoch mit dem *booleschen* Wert **TRUE** oder **FALSE** bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="14fbd-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="14fbd-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="14fbd-120">Example</span></span>

<span data-ttu-id="14fbd-121">`AND (1=1, "a"="a")` gibt **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="14fbd-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="14fbd-122">`AND (1=2, "a"="a")` gibt **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="14fbd-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14fbd-123">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="14fbd-123">Additional resources</span></span>

[<span data-ttu-id="14fbd-124">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="14fbd-124">Logical functions</span></span>](er-functions-category-logical.md)
