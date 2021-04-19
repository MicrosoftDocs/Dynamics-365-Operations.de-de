---
title: CH_BANK_MOD_10 EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der CH_BANK_MOD_10-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 92750ca7e7396077d8c56c3b336f495c228dddce
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744414"
---
# <a name="ch_bank_mod_10-er-function"></a><span data-ttu-id="050b8-103">CH_BANK_MOD_10 EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="050b8-103">CH_BANK_MOD_10 ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="050b8-104">Die Funktion `CH_BANK_MOD_10` gibt den Wert *String* zurück, der eine Gläubigerreferenz als MOD10-Ausdruck basierend auf den Ziffern der angegebenen Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="050b8-104">The `CH_BANK_MOD_10` function returns a *String* value that represents a creditor reference as an MOD10 expression, based on the digits of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="050b8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="050b8-105">Syntax</span></span>

```vb
CH_BANK_MOD_10 (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="050b8-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="050b8-106">Arguments</span></span>

<span data-ttu-id="050b8-107">`invoice number digits`: *String*</span><span class="sxs-lookup"><span data-stu-id="050b8-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="050b8-108">Ein Textwert, der die Ziffern einer Rechnungsnummer darstellt.</span><span class="sxs-lookup"><span data-stu-id="050b8-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="050b8-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="050b8-109">Return values</span></span>

<span data-ttu-id="050b8-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="050b8-110">*String*</span></span>

<span data-ttu-id="050b8-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="050b8-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="050b8-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="050b8-112">Example</span></span>

<span data-ttu-id="050b8-113">`CH_BANK_MOD_10 ("VEND-200002")` gibt **3** zurück.</span><span class="sxs-lookup"><span data-stu-id="050b8-113">`CH_BANK_MOD_10 ("VEND-200002")` returns **3**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="050b8-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="050b8-114">Additional resources</span></span>

[<span data-ttu-id="050b8-115">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="050b8-115">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]