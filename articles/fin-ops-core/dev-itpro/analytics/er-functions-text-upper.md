---
title: UPPER EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der UPPER-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: ed862ab823cfc3539c420d3066c9397e1e6d870e
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916682"
---
# <span data-ttu-id="e3255-103"><a name="UPPER">UPPER EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="e3255-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3255-104">Die Funktion `UPPER` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Großbuchstaben umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="e3255-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3255-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e3255-105">Syntax</span></span>

```
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="e3255-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="e3255-106">Arguments</span></span>

<span data-ttu-id="e3255-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="e3255-107">`text`: *String*</span></span>

<span data-ttu-id="e3255-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="e3255-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e3255-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e3255-109">Return values</span></span>

<span data-ttu-id="e3255-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="e3255-110">*String*</span></span>

<span data-ttu-id="e3255-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="e3255-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="e3255-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e3255-112">Example</span></span>

<span data-ttu-id="e3255-113">`UPPER ("Sample")` gibt **"SAMPLE"** zurück.</span><span class="sxs-lookup"><span data-stu-id="e3255-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3255-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e3255-114">Additional resources</span></span>

[<span data-ttu-id="e3255-115">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="e3255-115">Text functions</span></span>](er-functions-category-text.md)
