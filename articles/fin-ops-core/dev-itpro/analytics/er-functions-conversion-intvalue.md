---
title: INTVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von INTVALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c5c3e4c8bd918fa1154d2c111970d2f6d0e90e08
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743638"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="6c401-103">INTVALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="6c401-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c401-104">Die Funktion `INTVALUE` gibt den Wert *Int* zurück, der die angegebene Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="6c401-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="6c401-105">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="6c401-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="6c401-106">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="6c401-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="6c401-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="6c401-107">Arguments</span></span>

<span data-ttu-id="6c401-108">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="6c401-108">`text`: *String*</span></span>

<span data-ttu-id="6c401-109">Ein Textwert, der in die Zahl *Int* konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="6c401-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="6c401-110">`number`: *Real* oder *Integer*</span><span class="sxs-lookup"><span data-stu-id="6c401-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="6c401-111">Der numerische Wert *Real* oder *Integer*, der in die Zahl *Int* konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="6c401-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="6c401-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6c401-112">Return values</span></span>

<span data-ttu-id="6c401-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="6c401-113">*Int*</span></span>

<span data-ttu-id="6c401-114">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="6c401-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="6c401-115">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="6c401-115">Usage notes</span></span>

<span data-ttu-id="6c401-116">Sämtliche Dezimalstellen werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="6c401-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="6c401-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="6c401-117">Example 1</span></span>

<span data-ttu-id="6c401-118">`INTVALUE ("100.77")` gibt den *Int*-Wert **100** zurück.</span><span class="sxs-lookup"><span data-stu-id="6c401-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="6c401-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="6c401-119">Example 2</span></span>

<span data-ttu-id="6c401-120">`INTVALUE (-100.77)` gibt den *Int*-Wert **-100** zurück.</span><span class="sxs-lookup"><span data-stu-id="6c401-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c401-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6c401-121">Additional resources</span></span>

[<span data-ttu-id="6c401-122">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="6c401-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
