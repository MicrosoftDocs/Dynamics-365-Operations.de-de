---
title: LEN EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LEN-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e0ba19e762574dde4f9038b87ce352d13f714f4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041054"
---
# <span data-ttu-id="db3bc-103"><a name="LEN">LEN EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="db3bc-103"><a name="LEN">LEN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="db3bc-104">Die Funktion `LEN` gibt die angegebene Anzahl von Zeichen in der angegebenen Zeichenfolge mit dem Wert *Integer* zurück.</span><span class="sxs-lookup"><span data-stu-id="db3bc-104">The `LEN` function returns the number of characters in the specified string as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="db3bc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="db3bc-105">Syntax</span></span>

```vb
LEN (text)
```

## <a name="arguments"></a><span data-ttu-id="db3bc-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="db3bc-106">Arguments</span></span>

<span data-ttu-id="db3bc-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="db3bc-107">`text`: *String*</span></span>

<span data-ttu-id="db3bc-108">Der Wert *String*, der den Text angibt.</span><span class="sxs-lookup"><span data-stu-id="db3bc-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="db3bc-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="db3bc-109">Return values</span></span>

<span data-ttu-id="db3bc-110">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="db3bc-110">*Integer*</span></span>

<span data-ttu-id="db3bc-111">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="db3bc-111">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="db3bc-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="db3bc-112">Example</span></span>

<span data-ttu-id="db3bc-113">`LEN ("Sample")` gibt **6** zurück.</span><span class="sxs-lookup"><span data-stu-id="db3bc-113">`LEN ("Sample")` returns **6**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="db3bc-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="db3bc-114">Additional resources</span></span>

[<span data-ttu-id="db3bc-115">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="db3bc-115">Text functions</span></span>](er-functions-category-text.md)
