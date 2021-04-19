---
title: ISOCREDREF EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der ISOCREDREF-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 51adc6392b07ba4061a475f3072fb35452f15ad2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748316"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="5a74e-103">ISOCREDREF EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="5a74e-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a74e-104">Die Funktion `ISOCREDREF` gibt den Wert *String* zurück, der eine Gläubigerreferenz der Internationale Organisation für Normung (ISO) basierend auf den Ziffern und alphabetischen Symbolen der angegebenen Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a74e-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a74e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a74e-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="5a74e-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="5a74e-106">Arguments</span></span>

<span data-ttu-id="5a74e-107">`invoice number digits`: *String*</span><span class="sxs-lookup"><span data-stu-id="5a74e-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="5a74e-108">Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a74e-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="5a74e-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5a74e-109">Return values</span></span>

<span data-ttu-id="5a74e-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="5a74e-110">*String*</span></span>

<span data-ttu-id="5a74e-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="5a74e-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="5a74e-112">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="5a74e-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="5a74e-113">Um Symbole aus Alphabeten zu entfernen, die nicht ISO-kompatibel sind, muss das Argument `invoice number digits` übersetzt werden, bevor es an diese Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="5a74e-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="5a74e-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5a74e-114">Example</span></span>

<span data-ttu-id="5a74e-115">`ISOCredRef ("VEND-200002")` gibt **"RF23VEND-200002"** zurück.</span><span class="sxs-lookup"><span data-stu-id="5a74e-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a74e-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5a74e-116">Additional resources</span></span>

[<span data-ttu-id="5a74e-117">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="5a74e-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]