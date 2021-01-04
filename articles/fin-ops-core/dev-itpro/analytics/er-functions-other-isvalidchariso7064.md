---
title: ISVALIDCHARACTERISO7064 EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ISVALIDCHARACTERISO7064-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: c3bceb15bbe1dc65abc88c1229459707a6166482
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680661"
---
# <a name="isvalidcharacteriso7064-er-function"></a><span data-ttu-id="6b01d-103">ISVALIDCHARACTERISO7064 EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="6b01d-103">ISVALIDCHARACTERISO7064 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6b01d-104">Diese Funktion `ISVALIDCHARACTERISO7064` gibt den *booleschen* Wert **TRUE** zurück, wenn die angegebene Zeichenfolge eine gültige internationale Bankkontonummer (IBAN) darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b01d-104">The `ISVALIDCHARACTERISO7064` function returns a *Boolean* value of **TRUE** if the specified string represents a valid international bank account number (IBAN).</span></span> <span data-ttu-id="6b01d-105">Andernfalls gibt sie den *booleschen* Wert **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b01d-105">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b01d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6b01d-106">Syntax</span></span>

```vb
ISVALIDCHARACTERISO7064 (text)
```

## <a name="arguments"></a><span data-ttu-id="6b01d-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="6b01d-107">Arguments</span></span>

<span data-ttu-id="6b01d-108">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="6b01d-108">`text`: *String*</span></span>

<span data-ttu-id="6b01d-109">Ein Textwert, der eine IBAN darstellt.</span><span class="sxs-lookup"><span data-stu-id="6b01d-109">A text value that represents an IBAN.</span></span>

## <a name="return-values"></a><span data-ttu-id="6b01d-110">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="6b01d-110">Return values</span></span>

<span data-ttu-id="6b01d-111">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="6b01d-111">*String*</span></span>

<span data-ttu-id="6b01d-112">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="6b01d-112">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="6b01d-113">Beispiel</span><span class="sxs-lookup"><span data-stu-id="6b01d-113">Example</span></span>

<span data-ttu-id="6b01d-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` gibt **TRUE** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b01d-114">`ISVALIDCHARACTERISO7064 ("AT61 1904 3002 3457 3201")` returns **TRUE**.</span></span> 

<span data-ttu-id="6b01d-115">`ISVALIDCHARACTERISO7064 ("AT61")` gibt **FALSE** zurück.</span><span class="sxs-lookup"><span data-stu-id="6b01d-115">`ISVALIDCHARACTERISO7064 ("AT61")` returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6b01d-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="6b01d-116">Additional resources</span></span>

[<span data-ttu-id="6b01d-117">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="6b01d-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
