---
title: VALUE EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von VALUE bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 2252823d98b63d36d9bb195696abef34ac9c98b6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752579"
---
# <a name="value-er-function"></a><span data-ttu-id="74c3d-103">VALUE EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="74c3d-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74c3d-104">Diese Funktion `VALUE` gibt den Wert *Real* zurück, der über die angegebene Zeichenfolge konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="74c3d-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="74c3d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="74c3d-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="74c3d-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="74c3d-106">Arguments</span></span>

<span data-ttu-id="74c3d-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="74c3d-107">`text`: *String*</span></span>

<span data-ttu-id="74c3d-108">Ein Zeichenfolgewert, der in eine numerische Zahl konvertiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="74c3d-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="74c3d-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="74c3d-109">Return values</span></span>

<span data-ttu-id="74c3d-110">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="74c3d-110">*Real*</span></span>

<span data-ttu-id="74c3d-111">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="74c3d-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="74c3d-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="74c3d-112">Usage notes</span></span>

<span data-ttu-id="74c3d-113">Kommas und Punktzeichen (.) gelten als Dezimaltrennzeichen und es wird ein führender Bindestrich (-) als ein negatives Vorzeichen verwendet.</span><span class="sxs-lookup"><span data-stu-id="74c3d-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="74c3d-114">Eine Ausnahme wird bei der Laufzeit ausgelöst, wenn die angegebene Zeichenfolge andere nichtnumerische Zeichen enthält.</span><span class="sxs-lookup"><span data-stu-id="74c3d-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="74c3d-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="74c3d-115">Example 1</span></span>

<span data-ttu-id="74c3d-116">`VALUE ("1 234,56")` löst eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="74c3d-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="74c3d-117">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="74c3d-117">Example 2</span></span>

<span data-ttu-id="74c3d-118">`VALUE ("1234,56")` gibt **1234.56** zurück.</span><span class="sxs-lookup"><span data-stu-id="74c3d-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74c3d-119">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="74c3d-119">Additional resources</span></span>

[<span data-ttu-id="74c3d-120">Funktionen zur Typenumrechnung</span><span class="sxs-lookup"><span data-stu-id="74c3d-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]