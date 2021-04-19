---
title: AND EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von AND bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: 9851321137b4c7744634df30f85aa3a0b1a0a588
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745472"
---
# <a name="and-er-function"></a><span data-ttu-id="4ff79-103">AND EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="4ff79-103">AND ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ff79-104">Die Funktion `AND` gibt den *booleschen* Wert **TRUE** zurück, wenn alle angegebenen Bedingungen wahr sind.</span><span class="sxs-lookup"><span data-stu-id="4ff79-104">The `AND` function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="4ff79-105">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ff79-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ff79-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="4ff79-106">Syntax</span></span>

```vb
AND (condition 1[, condition 2, …, condition N])
```

## <a name="arguments"></a><span data-ttu-id="4ff79-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="4ff79-107">Arguments</span></span>

<span data-ttu-id="4ff79-108">`condition 1`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="4ff79-108">`condition 1`: *Boolean*</span></span>

<span data-ttu-id="4ff79-109">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="4ff79-109">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4ff79-110">Dieses Argument ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4ff79-110">This argument is required.</span></span>

<span data-ttu-id="4ff79-111">`condition N`: *Boolesch*</span><span class="sxs-lookup"><span data-stu-id="4ff79-111">`condition N`: *Boolean*</span></span>

<span data-ttu-id="4ff79-112">Ein gültiger Bedingungsausdruck, der getestet werden muss.</span><span class="sxs-lookup"><span data-stu-id="4ff79-112">A valid conditional expression that must be tested.</span></span> <span data-ttu-id="4ff79-113">Diese zusätzlichen Argumente sind optional.</span><span class="sxs-lookup"><span data-stu-id="4ff79-113">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="4ff79-114">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4ff79-114">Return values</span></span>

<span data-ttu-id="4ff79-115">*Aktiv*</span><span class="sxs-lookup"><span data-stu-id="4ff79-115">*Boolean*</span></span>

<span data-ttu-id="4ff79-116">Der resultierende *boolesche* Wert.</span><span class="sxs-lookup"><span data-stu-id="4ff79-116">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4ff79-117">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="4ff79-117">Usage notes</span></span>

<span data-ttu-id="4ff79-118">In den Argumenten logischer Funktionen können Sie Datenquellenverweise, numerische und Textwerte, Boolesche Werte, Vergleichsoperatoren und andere Funktionen für die elektronische Berichterstellung (EB) verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ff79-118">In the arguments of logical functions, you can use data source references, numeric and text values, Boolean values, comparison operators, and other Electronic reporting (ER) functions.</span></span> <span data-ttu-id="4ff79-119">Alle Argumente müssen jedoch mit dem *booleschen* Wert **TRUE** oder **FALSE** bewertet werden.</span><span class="sxs-lookup"><span data-stu-id="4ff79-119">However, all the arguments must be evaluated to a *Boolean* value of **TRUE** or **FALSE**.</span></span>

## <a name="example"></a><span data-ttu-id="4ff79-120">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4ff79-120">Example</span></span>

<span data-ttu-id="4ff79-121">`AND (1=1, "a"="a")` gibt **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ff79-121">`AND (1=1, "a"="a")` returns **TRUE**.</span></span>

<span data-ttu-id="4ff79-122">`AND (1=2, "a"="a")` gibt **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="4ff79-122">`AND (1=2, "a"="a")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4ff79-123">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4ff79-123">Additional resources</span></span>

[<span data-ttu-id="4ff79-124">Logische Funktionen</span><span class="sxs-lookup"><span data-stu-id="4ff79-124">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]