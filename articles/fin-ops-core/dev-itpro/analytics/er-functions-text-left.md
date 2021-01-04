---
title: LEFT EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LEFT-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 9e9cdff9bb5c22c74803cf17c056c0ff1af5ef43
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685882"
---
# <a name="left-er-function"></a><span data-ttu-id="4c5db-103">LEFT EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="4c5db-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4c5db-104">Die Funktion `LEFT` gibt den Wert *String* zurück, der die angegebene Anzahl von Zeichen ab dem Anfang der angegebenen Zeichenfolge angibt.</span><span class="sxs-lookup"><span data-stu-id="4c5db-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c5db-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c5db-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="4c5db-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="4c5db-106">Arguments</span></span>

<span data-ttu-id="4c5db-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="4c5db-107">`text`: *String*</span></span>

<span data-ttu-id="4c5db-108">Der Wert *String*, der den Originaltext darstellt.</span><span class="sxs-lookup"><span data-stu-id="4c5db-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="4c5db-109">`number`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="4c5db-109">`number`: *Integer*</span></span>

<span data-ttu-id="4c5db-110">Die Anzahl der Zeichen, die vom Start des Originaltexts zurückgegeben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="4c5db-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="4c5db-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4c5db-111">Return values</span></span>

<span data-ttu-id="4c5db-112">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="4c5db-112">*String*</span></span>

<span data-ttu-id="4c5db-113">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="4c5db-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="4c5db-114">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4c5db-114">Example</span></span>

<span data-ttu-id="4c5db-115">`LEFT ("Sample", 3)` gibt **"Sam"** zurück.</span><span class="sxs-lookup"><span data-stu-id="4c5db-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4c5db-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4c5db-116">Additional resources</span></span>

[<span data-ttu-id="4c5db-117">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="4c5db-117">Text functions</span></span>](er-functions-category-text.md)
