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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c9a75cedcf543b318df2850df3e4a60bac2dc6b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680685"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="db099-103">ISOCREDREF EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="db099-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db099-104">Die Funktion `ISOCREDREF` gibt den Wert *String* zurück, der eine Gläubigerreferenz der Internationale Organisation für Normung (ISO) basierend auf den Ziffern und alphabetischen Symbolen der angegebenen Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="db099-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="db099-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db099-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="db099-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="db099-106">Arguments</span></span>

<span data-ttu-id="db099-107">`invoice number digits`: *String*</span><span class="sxs-lookup"><span data-stu-id="db099-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="db099-108">Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="db099-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="db099-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="db099-109">Return values</span></span>

<span data-ttu-id="db099-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="db099-110">*String*</span></span>

<span data-ttu-id="db099-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="db099-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="db099-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="db099-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="db099-113">Um Symbole aus Alphabeten zu entfernen, die nicht ISO-kompatibel sind, muss das Argument `invoice number digits` übersetzt werden, bevor es an diese Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="db099-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="db099-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="db099-114">Example</span></span>

<span data-ttu-id="db099-115">`ISOCredRef ("VEND-200002")` gibt **"RF23VEND-200002"** zurück.</span><span class="sxs-lookup"><span data-stu-id="db099-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db099-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db099-116">Additional resources</span></span>

[<span data-ttu-id="db099-117">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="db099-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
