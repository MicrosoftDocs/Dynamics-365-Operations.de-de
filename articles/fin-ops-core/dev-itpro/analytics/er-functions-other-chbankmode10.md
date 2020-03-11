---
title: CH_BANK_MOD_10 EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CH_BANK_MOD_10-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 808e328bfcc35c96091da9a69850429b82a71070
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070574"
---
# <span data-ttu-id="a3d35-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="a3d35-103"><a name="CH_BANK_MOD_10">CH_BANK_MOD_10 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3d35-104">Die Funktion `CH_BANK_MOD_10` gibt den Wert *String* zurück, der eine Gläubigerreferenz als MOD10-Ausdruck basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3d35-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="a3d35-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3d35-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="a3d35-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="a3d35-106">Arguments</span></span>

<span data-ttu-id="a3d35-107">`invoice number digits`: *String*</span><span class="sxs-lookup"><span data-stu-id="a3d35-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="a3d35-108">Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="a3d35-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="a3d35-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="a3d35-109">Return values</span></span>

<span data-ttu-id="a3d35-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="a3d35-110">*String*</span></span>

<span data-ttu-id="a3d35-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="a3d35-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="a3d35-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="a3d35-112">Example</span></span>

<span data-ttu-id="a3d35-113">`CH_BANK_MOD_10 ("VEND-200002")` gibt **3** zurück.</span><span class="sxs-lookup"><span data-stu-id="a3d35-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a3d35-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="a3d35-114">Additional resources</span></span>

[<span data-ttu-id="a3d35-115">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="a3d35-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
