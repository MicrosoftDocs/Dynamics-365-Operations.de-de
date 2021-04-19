---
title: ABS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ABS-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: 2a3613483d53fb265741b5d6a34a91da443dcef7
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753143"
---
# <a name="abs-er-function"></a><span data-ttu-id="94f60-103">ABS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="94f60-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="94f60-104">Die Funktion `ABS` gibt den absoluten Wert (Modulus) der angegebenen Zahl mit dem Wert *Real* zurück.</span><span class="sxs-lookup"><span data-stu-id="94f60-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="94f60-105">In anderen Worten gibt sie die Zahl ohne das Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="94f60-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="94f60-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="94f60-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="94f60-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="94f60-107">Arguments</span></span>

<span data-ttu-id="94f60-108">`number`: *Real*</span><span class="sxs-lookup"><span data-stu-id="94f60-108">`number`: *Real*</span></span>

<span data-ttu-id="94f60-109">Ein numerischer Wert, dessen Modul Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="94f60-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="94f60-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="94f60-110">Return values</span></span>

<span data-ttu-id="94f60-111">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="94f60-111">*Real*</span></span>

<span data-ttu-id="94f60-112">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="94f60-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="94f60-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="94f60-113">Example</span></span>

<span data-ttu-id="94f60-114">`ABS (-1)` gibt **1** zurück.</span><span class="sxs-lookup"><span data-stu-id="94f60-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="94f60-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="94f60-115">Additional resources</span></span>

[<span data-ttu-id="94f60-116">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="94f60-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]