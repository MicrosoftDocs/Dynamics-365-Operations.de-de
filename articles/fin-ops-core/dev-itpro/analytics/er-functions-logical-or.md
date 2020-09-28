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
ms.openlocfilehash: faf07c5d8b30cd3babe8a6a55ae7effe5ce457a0
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744622"
---
# <a name="or-er-function"></a><span data-ttu-id="4e7a1-103">OR EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="4e7a1-103">OR ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4e7a1-104">Die Funktion `OR` gibt den *booleschen* Wert **FALSE** zurück, wenn alle angegebenen Bedingungen falsch sind.</span><span class="sxs-lookup"><span data-stu-id="4e7a1-104">The `OR` function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="4e7a1-105">Wenn eine der angegebenen Bedingungen wahr ist, gibt die Funktion den *booleschen* Wert **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e7a1-105">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e7a1-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4e7a1-106">Syntax</span></span>

```vb
OR (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="4e7a1-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="4e7a1-107">Arguments</span></span>

<span data-ttu-id="4e7a1-108">`condition 1`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="4e7a1-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="4e7a1-109">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="4e7a1-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4e7a1-110">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4e7a1-110">This argument is required.</span></span>

<span data-ttu-id="4e7a1-111">`condition N`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="4e7a1-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="4e7a1-112">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="4e7a1-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4e7a1-113">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="4e7a1-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4e7a1-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4e7a1-114">Return values</span></span>

<span data-ttu-id="4e7a1-115">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="4e7a1-115">*Boolean*</span></span>

<span data-ttu-id="4e7a1-116">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="4e7a1-116">The resulting *Boolean* value.</span></span>

## <a name="example"></a><span data-ttu-id="4e7a1-117">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4e7a1-117">Example</span></span>

<span data-ttu-id="4e7a1-118">`OR (1=2, "a"="a")` gibt **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="4e7a1-118">`OR (1=2, "a"="a")` returns **TRUE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4e7a1-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4e7a1-119">Additional resources</span></span>

[<span data-ttu-id="4e7a1-120">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4e7a1-120">Logical functions</span></span>](er-functions-category-logical.md)
