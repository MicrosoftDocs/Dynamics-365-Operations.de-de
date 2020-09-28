---
title: NUMBERVALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von NUMBERVALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 13346c4810d6c93d4ef47ce525831332562c7f51
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743398"
---
# <a name="numbervalue-er-function"></a><span data-ttu-id="b7114-103">NUMBERVALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="b7114-103">NUMBERVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7114-104">Diese Funktion `NUMBERVALUE` gibt den Wert *Real* zurück, der über den angegebenen Wert *String* konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="b7114-104">The `NUMBERVALUE` function returns a *Real* value that is converted from the specified *String* value.</span></span> <span data-ttu-id="b7114-105">Bei der Konvertierung werden die angegebenen Trennzeichen für Dezimal- und Zifferngruppierungen berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="b7114-105">During the conversion, the specified decimal and digit grouping separators are considered.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7114-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="b7114-106">Syntax</span></span>

```vb
NUMBERVALUE (text, decimal separator, digit grouping separator)
```

## <a name="arguments"></a><span data-ttu-id="b7114-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="b7114-107">Arguments</span></span>

<span data-ttu-id="b7114-108">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="b7114-108">`text`: *String*</span></span>

<span data-ttu-id="b7114-109">Ein Textwert, der in die Zahl *Real* konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="b7114-109">A text value that must be converted to a *Real* number.</span></span>

<span data-ttu-id="b7114-110">`decimal separator`: String</span><span class="sxs-lookup"><span data-stu-id="b7114-110">`decimal separator`: String</span></span>

<span data-ttu-id="b7114-111">Ein Dezimaltrennzeichen.</span><span class="sxs-lookup"><span data-stu-id="b7114-111">A decimal separator.</span></span> <span data-ttu-id="b7114-112">Es wird verwendet, um die ganze Zahl und die Bruchteile einer Dezimalzahl zu trennen.</span><span class="sxs-lookup"><span data-stu-id="b7114-112">It's used to separate the integer and fractional parts of a decimal number.</span></span>

<span data-ttu-id="b7114-113">`digit grouping separator`: *String*</span><span class="sxs-lookup"><span data-stu-id="b7114-113">`digit grouping separator`: *String*</span></span>

<span data-ttu-id="b7114-114">Ein Trennzeichen für Zifferngruppen.</span><span class="sxs-lookup"><span data-stu-id="b7114-114">A digit grouping separator.</span></span> <span data-ttu-id="b7114-115">Es wird als Tausendertrennzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b7114-115">It's used as the thousands separator.</span></span>

## <a name="return-values"></a><span data-ttu-id="b7114-116">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b7114-116">Return values</span></span>

<span data-ttu-id="b7114-117">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="b7114-117">*Real*</span></span>

<span data-ttu-id="b7114-118">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="b7114-118">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="b7114-119">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b7114-119">Example</span></span>

<span data-ttu-id="b7114-120">`NUMBERVALUE( "1 234,56", ",", " ")` gibt **1234.56** zurück.</span><span class="sxs-lookup"><span data-stu-id="b7114-120">`NUMBERVALUE( "1 234,56", ",", " ")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b7114-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b7114-121">Additional resources</span></span>

[<span data-ttu-id="b7114-122">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="b7114-122">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
