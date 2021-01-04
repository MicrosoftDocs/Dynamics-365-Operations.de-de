---
title: INT64VALUE ER Funktion
description: In diesem Thema werden Informationen zur Verwendung von INT64VALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bb750116312df82448f5a0048e380f9e5274f8e9
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686050"
---
# <a name="int64value-er-function"></a><span data-ttu-id="1c735-103">INT64VALUE ER Funktion</span><span class="sxs-lookup"><span data-stu-id="1c735-103">INT64VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1c735-104">Die Funktion `INT64VALUE` gibt den Wert *Int64* zurück, der die angegebene Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="1c735-104">The `INT64VALUE` function returns an *Int64* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="1c735-105">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="1c735-105">Syntax 1</span></span>

```vb
INT64VALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="1c735-106">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="1c735-106">Syntax 2</span></span>

```vb
INT64VALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="1c735-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="1c735-107">Arguments</span></span>

<span data-ttu-id="1c735-108">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="1c735-108">`text`: *String*</span></span>

<span data-ttu-id="1c735-109">Ein Textwert, der in die Zahl *Int64* konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="1c735-109">A text value that must be converted to an *Int64* number.</span></span>

<span data-ttu-id="1c735-110">`number`: *Real* oder *Integer*</span><span class="sxs-lookup"><span data-stu-id="1c735-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="1c735-111">Der numerische Wert *Real* oder *Integer*, der in die Zahl *Int64* konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="1c735-111">A numeric *Real* or *Integer* value that must be converted to an *Int64* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="1c735-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="1c735-112">Return values</span></span>

<span data-ttu-id="1c735-113">*Int64*</span><span class="sxs-lookup"><span data-stu-id="1c735-113">*Int64*</span></span>

<span data-ttu-id="1c735-114">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="1c735-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1c735-115">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="1c735-115">Usage notes</span></span>

<span data-ttu-id="1c735-116">Sämtliche Dezimalstellen werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="1c735-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="1c735-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c735-117">Example 1</span></span>

<span data-ttu-id="1c735-118">`INT64VALUE ("22565422744")` gibt den *Int64*-Wert **22565422744** zurück.</span><span class="sxs-lookup"><span data-stu-id="1c735-118">`INT64VALUE ("22565422744")` returns the *Int64* value **22565422744**.</span></span>

## <a name="example-2"></a><span data-ttu-id="1c735-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1c735-119">Example 2</span></span>

<span data-ttu-id="1c735-120">`INT64VALUE ( VALUE("22565422744.77"))` gibt den *Int64*-Wert **22565422744** zurück.</span><span class="sxs-lookup"><span data-stu-id="1c735-120">`INT64VALUE ( VALUE("22565422744.77"))` returns the *Int64* value **22565422744**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1c735-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="1c735-121">Additional resources</span></span>

[<span data-ttu-id="1c735-122">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="1c735-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
