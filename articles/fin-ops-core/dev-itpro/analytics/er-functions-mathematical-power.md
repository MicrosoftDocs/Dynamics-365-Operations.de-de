---
title: POWER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der POWER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 080b2f9b1ada55209c9470386aceab2d3ef456af
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744574"
---
# <a name="power-er-function"></a><span data-ttu-id="f8d43-103">POWER EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="f8d43-103">POWER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8d43-104">Die Funktion `POWER` gibt den Wert *Real* zurück, der das Ergebnis der Erhöhung der angegebenen positiven Zahl auf die angegebene Potenz darstellt.</span><span class="sxs-lookup"><span data-stu-id="f8d43-104">The `POWER` function returns a *Real* value that represents the result of raising the specified positive number to the specified power.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8d43-105">Syntax</span></span>

```vb
POWER (number, power)
```

## <a name="arguments"></a><span data-ttu-id="f8d43-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="f8d43-106">Arguments</span></span>

<span data-ttu-id="f8d43-107">`number`: *Real* oder *Integer*</span><span class="sxs-lookup"><span data-stu-id="f8d43-107">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="f8d43-108">Ein numerischer Wert, der auf die angegebene Potenz angehoben werden muss.</span><span class="sxs-lookup"><span data-stu-id="f8d43-108">A numeric value that must be raised to the specified power.</span></span>

<span data-ttu-id="f8d43-109">`power`: *Real* oder *Integer*</span><span class="sxs-lookup"><span data-stu-id="f8d43-109">`power`: *Real* or *Integer*</span></span>

<span data-ttu-id="f8d43-110">Ein numerischer Wert, der die spezifische Potenz darstellt.</span><span class="sxs-lookup"><span data-stu-id="f8d43-110">A numeric value that represents the specific power.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8d43-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f8d43-111">Return values</span></span>

<span data-ttu-id="f8d43-112">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="f8d43-112">*Real*</span></span>

<span data-ttu-id="f8d43-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="f8d43-113">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="f8d43-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8d43-114">Example 1</span></span>

<span data-ttu-id="f8d43-115">`POWER (10, 2)` gibt **100** zurück.</span><span class="sxs-lookup"><span data-stu-id="f8d43-115">`POWER (10, 2)` returns **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="f8d43-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f8d43-116">Example 2</span></span>

<span data-ttu-id="f8d43-117">`POWER (4, 0.5)` gibt **2** zurück.</span><span class="sxs-lookup"><span data-stu-id="f8d43-117">`POWER (4, 0.5)` returns **2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8d43-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f8d43-118">Additional resources</span></span>

[<span data-ttu-id="f8d43-119">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="f8d43-119">Mathematical functions</span></span>](er-functions-category-mathematical.md)
