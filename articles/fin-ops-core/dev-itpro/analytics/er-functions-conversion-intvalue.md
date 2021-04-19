---
title: INTVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von INTVALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 71eedde5a22f36a8a827824087633de32c00cc7d
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755371"
---
# <a name="intvalue-er-function"></a><span data-ttu-id="337cd-103">INTVALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="337cd-103">INTVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="337cd-104">Die Funktion `INTVALUE` gibt den Wert *Int* zurück, der die angegebene Zeichenfolge darstellt.</span><span class="sxs-lookup"><span data-stu-id="337cd-104">The `INTVALUE` function returns an *Int* value that represents the specified string.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="337cd-105">Syntax 1</span><span class="sxs-lookup"><span data-stu-id="337cd-105">Syntax 1</span></span>

```vb
INTVALUE (text)
```

## <a name="syntax-2"></a><span data-ttu-id="337cd-106">Syntax 2</span><span class="sxs-lookup"><span data-stu-id="337cd-106">Syntax 2</span></span>

```vb
INTVALUE (number)
```

## <a name="arguments"></a><span data-ttu-id="337cd-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="337cd-107">Arguments</span></span>

<span data-ttu-id="337cd-108">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="337cd-108">`text`: *String*</span></span>

<span data-ttu-id="337cd-109">Ein Textwert, der in die Zahl *Int* konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="337cd-109">A text value that must be converted to an *Int* number.</span></span>

<span data-ttu-id="337cd-110">`number`: *Real* oder *Integer*</span><span class="sxs-lookup"><span data-stu-id="337cd-110">`number`: *Real* or *Integer*</span></span>

<span data-ttu-id="337cd-111">Der numerische Wert *Real* oder *Integer*, der in die Zahl *Int* konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="337cd-111">A numeric *Real* or *Integer* value that must be converted to an *Int* number.</span></span>

## <a name="return-values"></a><span data-ttu-id="337cd-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="337cd-112">Return values</span></span>

<span data-ttu-id="337cd-113">*Int*</span><span class="sxs-lookup"><span data-stu-id="337cd-113">*Int*</span></span>

<span data-ttu-id="337cd-114">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="337cd-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="337cd-115">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="337cd-115">Usage notes</span></span>

<span data-ttu-id="337cd-116">Sämtliche Dezimalstellen werden abgeschnitten.</span><span class="sxs-lookup"><span data-stu-id="337cd-116">Any decimal places are truncated.</span></span>

## <a name="example-1"></a><span data-ttu-id="337cd-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="337cd-117">Example 1</span></span>

<span data-ttu-id="337cd-118">`INTVALUE ("100.77")` gibt den *Int*-Wert **100** zurück.</span><span class="sxs-lookup"><span data-stu-id="337cd-118">`INTVALUE ("100.77")` returns the *Int* value **100**.</span></span>

## <a name="example-2"></a><span data-ttu-id="337cd-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="337cd-119">Example 2</span></span>

<span data-ttu-id="337cd-120">`INTVALUE (-100.77)` gibt den *Int*-Wert **-100** zurück.</span><span class="sxs-lookup"><span data-stu-id="337cd-120">`INTVALUE (-100.77)` returns the *Int* value **-100**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="337cd-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="337cd-121">Additional resources</span></span>

[<span data-ttu-id="337cd-122">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="337cd-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]