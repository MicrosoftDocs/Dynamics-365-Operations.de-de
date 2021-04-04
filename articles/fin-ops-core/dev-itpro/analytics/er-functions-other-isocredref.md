---
title: ISOCREDREF EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ISOCREDREF-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: a9378028a4b308aae7796b861b37a5f89ddfe49c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563408"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="c3a9d-103">ISOCREDREF EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="c3a9d-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3a9d-104">Die Funktion `ISOCREDREF` gibt den Wert *String* zurück, der eine Gläubigerreferenz der Internationale Organisation für Normung (ISO) basierend auf den Ziffern und alphabetischen Symbolen der angegebenen Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3a9d-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3a9d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c3a9d-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="c3a9d-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="c3a9d-106">Arguments</span></span>

<span data-ttu-id="c3a9d-107">`invoice number digits`: *String*</span><span class="sxs-lookup"><span data-stu-id="c3a9d-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="c3a9d-108">Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="c3a9d-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="c3a9d-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="c3a9d-109">Return values</span></span>

<span data-ttu-id="c3a9d-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="c3a9d-110">*String*</span></span>

<span data-ttu-id="c3a9d-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="c3a9d-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="c3a9d-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="c3a9d-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="c3a9d-113">Um Symbole aus Alphabeten zu entfernen, die nicht ISO-kompatibel sind, muss das Argument `invoice number digits` übersetzt werden, bevor es an diese Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="c3a9d-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="c3a9d-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="c3a9d-114">Example</span></span>

<span data-ttu-id="c3a9d-115">`ISOCredRef ("VEND-200002")` gibt **"RF23VEND-200002"** zurück.</span><span class="sxs-lookup"><span data-stu-id="c3a9d-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3a9d-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="c3a9d-116">Additional resources</span></span>

[<span data-ttu-id="c3a9d-117">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="c3a9d-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]