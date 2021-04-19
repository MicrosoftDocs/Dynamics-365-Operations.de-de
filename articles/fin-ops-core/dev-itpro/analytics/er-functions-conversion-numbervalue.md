---
title: NUMBERVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von NUMBERVALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 84d7f17f37a83547522cf09047b72100f6f5b859
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755347"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="beec7-103">NUMBERVALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="beec7-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="beec7-104">Diese Funktion `NUMBERVALUE` gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="beec7-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="beec7-105">Bei der Konvertierung werden die angegebenen Trennzeichen für Dezimal- und Zifferngruppierungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="beec7-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="beec7-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="beec7-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="beec7-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="beec7-107">Arguments</span></span>

<span data-ttu-id="beec7-108">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="beec7-108">`text`: *String*</span></span>

<span data-ttu-id="beec7-109">Ein Textwert, der in die Zahl *Real* konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="beec7-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="beec7-110">`decimal separator`: String</span><span class="sxs-lookup"><span data-stu-id="beec7-110">`decimal separator`: String</span></span>

<span data-ttu-id="beec7-111">Ein Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="beec7-111">A decimal separator.</span></span> <span data-ttu-id="beec7-112">Es wird verwendet, um die ganze Zahl und die Bruchteile einer Dezimalzahl zu trennen.</span><span class="sxs-lookup"><span data-stu-id="beec7-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="beec7-113">`digit grouping separator`: *String*</span><span class="sxs-lookup"><span data-stu-id="beec7-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="beec7-114">Ein Trennzeichen für Zifferngruppen.</span><span class="sxs-lookup"><span data-stu-id="beec7-114">A digit grouping separator.</span></span> <span data-ttu-id="beec7-115">Es wird als Tausendertrennzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="beec7-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="beec7-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="beec7-116">Return values</span></span>

<span data-ttu-id="beec7-117">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="beec7-117">*Real*</span></span>

<span data-ttu-id="beec7-118">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="beec7-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="beec7-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="beec7-119">Example</span></span>

<span data-ttu-id="beec7-120">`NUMBERVALUE( "1 234,56", ",", " ")` gibt **1234.56** zurück.</span><span class="sxs-lookup"><span data-stu-id="beec7-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="beec7-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="beec7-121">Additional resources</span></span>

[<span data-ttu-id="beec7-122">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="beec7-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]