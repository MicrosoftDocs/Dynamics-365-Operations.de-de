---
title: ABS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ABS-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: 12165174806395b3c36a1dbb227ed7a86def77b1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5565783"
---
# <a name="abs-er-function"></a><span data-ttu-id="9895f-103">ABS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="9895f-103">ABS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9895f-104">Die Funktion `ABS` gibt den absoluten Wert (Modulus) der angegebenen Zahl mit dem Wert *Real* zurück.</span><span class="sxs-lookup"><span data-stu-id="9895f-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="9895f-105">In anderen Worten gibt sie die Zahl ohne das Vorzeichen zurück.</span><span class="sxs-lookup"><span data-stu-id="9895f-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="9895f-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="9895f-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="9895f-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="9895f-107">Arguments</span></span>

<span data-ttu-id="9895f-108">`number`: *Real*</span><span class="sxs-lookup"><span data-stu-id="9895f-108">`number`: *Real*</span></span>

<span data-ttu-id="9895f-109">Ein numerischer Wert, dessen Modul Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="9895f-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="9895f-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="9895f-110">Return values</span></span>

<span data-ttu-id="9895f-111">*Gleitkommazahl*</span><span class="sxs-lookup"><span data-stu-id="9895f-111">*Real*</span></span>

<span data-ttu-id="9895f-112">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="9895f-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="9895f-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="9895f-113">Example</span></span>

<span data-ttu-id="9895f-114">`ABS (-1)` gibt **1** zurück.</span><span class="sxs-lookup"><span data-stu-id="9895f-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9895f-115">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="9895f-115">Additional resources</span></span>

[<span data-ttu-id="9895f-116">Rechenoperationen</span><span class="sxs-lookup"><span data-stu-id="9895f-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]