---
title: VALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von VALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: ecbffb7e39d7f2f2bccdfe32d593512a65da163c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745512"
---
# <a name="value-er-function"></a><span data-ttu-id="811ee-103">VALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="811ee-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="811ee-104">Diese Funktion `VALUE` gibt den Wert *Real* zurück, der über die angegebene Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="811ee-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="811ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="811ee-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="811ee-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="811ee-106">Arguments</span></span>

<span data-ttu-id="811ee-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="811ee-107">`text`: *String*</span></span>

<span data-ttu-id="811ee-108">Ein Zeichenfolgewert, der in eine numerische Zahl konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="811ee-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="811ee-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="811ee-109">Return values</span></span>

<span data-ttu-id="811ee-110">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="811ee-110">*Real*</span></span>

<span data-ttu-id="811ee-111">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="811ee-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="811ee-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="811ee-112">Usage notes</span></span>

<span data-ttu-id="811ee-113">Kommas und Punktzeichen (.) gelten als Dezimaltrennzeichen und es wird ein führender Bindestrich (-) als ein negatives Vorzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="811ee-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="811ee-114">Eine Ausnahme wird bei der Laufzeit ausgelöst, wenn die angegebene Zeichenfolge andere nichtnumerische Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="811ee-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="811ee-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="811ee-115">Example 1</span></span>

<span data-ttu-id="811ee-116">`VALUE ("1 234,56")` löst eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="811ee-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="811ee-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="811ee-117">Example 2</span></span>

<span data-ttu-id="811ee-118">`VALUE ("1234,56")` gibt **1234.56** zurück.</span><span class="sxs-lookup"><span data-stu-id="811ee-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="811ee-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="811ee-119">Additional resources</span></span>

[<span data-ttu-id="811ee-120">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="811ee-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
