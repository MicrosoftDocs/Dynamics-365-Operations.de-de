---
title: MOD_97 EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der MOD_97-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: ce2192c7bc849996e08573d71d8ed43956c8fb89
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070528"
---
# <span data-ttu-id="4c5f3-103"><a name="MOD_97">MOD_97 EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="4c5f3-103"><a name="MOD_97">MOD_97 ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c5f3-104">Die Funktion `MOD_97` gibt den Wert *String* zurück, der eine Gläubigerreferenz als MOD97-Ausdruck basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="4c5f3-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5f3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c5f3-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="4c5f3-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="4c5f3-106">Arguments</span></span>

<span data-ttu-id="4c5f3-107">`invoice number digits`: *String*</span><span class="sxs-lookup"><span data-stu-id="4c5f3-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="4c5f3-108">Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="4c5f3-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="4c5f3-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4c5f3-109">Return values</span></span>

<span data-ttu-id="4c5f3-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="4c5f3-110">*String*</span></span>

<span data-ttu-id="4c5f3-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="4c5f3-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4c5f3-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4c5f3-112">Example</span></span>

<span data-ttu-id="4c5f3-113">`MOD_97 ("VEND-200002")` gibt **"20000285"** zurück.</span><span class="sxs-lookup"><span data-stu-id="4c5f3-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c5f3-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4c5f3-114">Additional resources</span></span>

[<span data-ttu-id="4c5f3-115">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="4c5f3-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
