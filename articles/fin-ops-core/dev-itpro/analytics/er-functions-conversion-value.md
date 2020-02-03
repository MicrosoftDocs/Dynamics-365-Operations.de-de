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
ms.openlocfilehash: 160dd81baa43702b2deea1e3eea20080fca122ca
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917625"
---
# <span data-ttu-id="e15c1-103"><a name="VALUE">VALUE EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="e15c1-103"><a name="VALUE">VALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e15c1-104">Diese Funktion `VALUE` gibt den Wert *Real* zurück, der über die angegebene Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="e15c1-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15c1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e15c1-105">Syntax</span></span>

```
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="e15c1-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="e15c1-106">Arguments</span></span>

<span data-ttu-id="e15c1-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="e15c1-107">`text`: *String*</span></span>

<span data-ttu-id="e15c1-108">Ein Zeichenfolgewert, der in eine numerische Zahl konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="e15c1-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="e15c1-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e15c1-109">Return values</span></span>

<span data-ttu-id="e15c1-110">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="e15c1-110">*Real*</span></span>

<span data-ttu-id="e15c1-111">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="e15c1-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e15c1-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="e15c1-112">Usage notes</span></span>

<span data-ttu-id="e15c1-113">Kommas und Punktzeichen (.) gelten als Dezimaltrennzeichen und es wird ein führender Bindestrich (-) als ein negatives Vorzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="e15c1-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="e15c1-114">Eine Ausnahme wird bei der Laufzeit ausgelöst, wenn die angegebene Zeichenfolge andere nichtnumerische Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="e15c1-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="e15c1-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="e15c1-115">Example 1</span></span>

<span data-ttu-id="e15c1-116">`VALUE ("1 234,56")` löst eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="e15c1-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="e15c1-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="e15c1-117">Example 2</span></span>

<span data-ttu-id="e15c1-118">`VALUE ("1234,56")` gibt **1234.56** zurück.</span><span class="sxs-lookup"><span data-stu-id="e15c1-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e15c1-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e15c1-119">Additional resources</span></span>

[<span data-ttu-id="e15c1-120">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="e15c1-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)