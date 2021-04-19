---
title: UPPER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der UPPER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 0e0e9837765914c657a72c5ce04c6f565fa13788
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749140"
---
# <a name="upper-er-function"></a><span data-ttu-id="b021d-103">UPPER EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="b021d-103">UPPER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b021d-104">Die Funktion `UPPER` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Großbuchstaben umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="b021d-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="b021d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b021d-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="b021d-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="b021d-106">Arguments</span></span>

<span data-ttu-id="b021d-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="b021d-107">`text`: *String*</span></span>

<span data-ttu-id="b021d-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="b021d-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="b021d-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b021d-109">Return values</span></span>

<span data-ttu-id="b021d-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="b021d-110">*String*</span></span>

<span data-ttu-id="b021d-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="b021d-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="b021d-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b021d-112">Example</span></span>

<span data-ttu-id="b021d-113">`UPPER ("Sample")` gibt **"SAMPLE"** zurück.</span><span class="sxs-lookup"><span data-stu-id="b021d-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b021d-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b021d-114">Additional resources</span></span>

[<span data-ttu-id="b021d-115">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="b021d-115">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]