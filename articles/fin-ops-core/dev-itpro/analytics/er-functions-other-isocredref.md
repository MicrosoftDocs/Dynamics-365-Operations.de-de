---
title: ISOCREDREF EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ISOCREDREF-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: ea72d824d3a98d7685a965e981d057991f012a0e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916958"
---
# <span data-ttu-id="e2f8c-103"><a name="ISOCREDREF">ISOCREDREF EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="e2f8c-103"><a name="ISOCREDREF">ISOCREDREF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2f8c-104">Die Funktion `ISOCREDREF` gibt den Wert *String* zurück, der eine Gläubigerreferenz der Internationale Organisation für Normung (ISO) basierend auf den Ziffern und alphabetischen Symbolen der angegebenen Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2f8c-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f8c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e2f8c-105">Syntax</span></span>

```
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="e2f8c-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="e2f8c-106">Arguments</span></span>

<span data-ttu-id="e2f8c-107">`invoice number digits`: *String*</span><span class="sxs-lookup"><span data-stu-id="e2f8c-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="e2f8c-108">Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2f8c-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="e2f8c-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e2f8c-109">Return values</span></span>

<span data-ttu-id="e2f8c-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e2f8c-110">*String*</span></span>

<span data-ttu-id="e2f8c-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="e2f8c-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e2f8c-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="e2f8c-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="e2f8c-113">Um Symbole aus Alphabeten zu entfernen, die nicht ISO-kompatibel sind, muss das Argument `invoice number digits` übersetzt werden, bevor es an diese Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="e2f8c-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="e2f8c-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e2f8c-114">Example</span></span>

<span data-ttu-id="e2f8c-115">`ISOCredRef ("VEND-200002")` gibt **"RF23VEND-200002"** zurück.</span><span class="sxs-lookup"><span data-stu-id="e2f8c-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e2f8c-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e2f8c-116">Additional resources</span></span>

[<span data-ttu-id="e2f8c-117">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="e2f8c-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
