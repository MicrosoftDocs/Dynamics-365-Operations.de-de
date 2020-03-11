---
title: LOWER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der LOWER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 6784384bac31d8c7cdc9c6f71b7dbab79c15a934
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041100"
---
# <span data-ttu-id="439ee-103"><a name="LOWER">LOWER EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="439ee-103"><a name="LOWER">LOWER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="439ee-104">Die Funktion `LOWER` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Kleinbuchstaben umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="439ee-104">The `LOWER` function returns the specified text string as a *String* value after it has been converted to lowercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="439ee-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="439ee-105">Syntax</span></span>

```vb
LOWER (text)
```

## <a name="arguments"></a><span data-ttu-id="439ee-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="439ee-106">Arguments</span></span>

<span data-ttu-id="439ee-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="439ee-107">`text`: *String*</span></span>

<span data-ttu-id="439ee-108">Der Wert *String*, der den Text angibt.</span><span class="sxs-lookup"><span data-stu-id="439ee-108">A *String* value that specifies the text.</span></span>

## <a name="return-values"></a><span data-ttu-id="439ee-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="439ee-109">Return values</span></span>

<span data-ttu-id="439ee-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="439ee-110">*String*</span></span>

<span data-ttu-id="439ee-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="439ee-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="439ee-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="439ee-112">Example</span></span>

<span data-ttu-id="439ee-113">`LOWER ("Sample")` gibt **"sample"** zurück.</span><span class="sxs-lookup"><span data-stu-id="439ee-113">`LOWER ("Sample")` returns **"sample"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="439ee-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="439ee-114">Additional resources</span></span>

[<span data-ttu-id="439ee-115">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="439ee-115">Text functions</span></span>](er-functions-category-text.md)
