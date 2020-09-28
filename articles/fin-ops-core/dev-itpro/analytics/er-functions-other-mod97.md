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
ms.openlocfilehash: b58e06a034fc6d26c891b78c26ac53c87a39b92b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744046"
---
# <a name="mod_97-er-function"></a><span data-ttu-id="5a083-103">MOD_97 EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="5a083-103">MOD_97 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a083-104">Die Funktion `MOD_97` gibt den Wert *String* zurück, der eine Gläubigerreferenz als MOD97-Ausdruck basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a083-104">The `MOD_97` function returns a *String* value that represents a creditor reference as a MOD97 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a083-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a083-105">Syntax</span></span>

```vb
MOD_97 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="5a083-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="5a083-106">Arguments</span></span>

<span data-ttu-id="5a083-107">`invoice number digits`: *String*</span><span class="sxs-lookup"><span data-stu-id="5a083-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="5a083-108">Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="5a083-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="5a083-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="5a083-109">Return values</span></span>

<span data-ttu-id="5a083-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="5a083-110">*String*</span></span>

<span data-ttu-id="5a083-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="5a083-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5a083-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5a083-112">Example</span></span>

<span data-ttu-id="5a083-113">`MOD_97 ("VEND-200002")` gibt **"20000285"** zurück.</span><span class="sxs-lookup"><span data-stu-id="5a083-113">`MOD_97 ("VEND-200002")` returns **"20000285"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5a083-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="5a083-114">Additional resources</span></span>

[<span data-ttu-id="5a083-115">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="5a083-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
