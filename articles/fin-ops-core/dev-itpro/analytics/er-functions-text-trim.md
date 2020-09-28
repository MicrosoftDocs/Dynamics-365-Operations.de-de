---
title: TRIM EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der TRIM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: a1f7999ccbcd167280cca1abc48377c36d2bc15f
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744214"
---
# <a name="trim-er-function"></a><span data-ttu-id="24423-103">TRIM EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="24423-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="24423-104">Die Funktion `TRIM` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem führende und nachfolgende Leerzeichen abgeschnitten wurden und nachdem mehrfache Leerzeichen zwischen Wörtern entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="24423-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="24423-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="24423-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="24423-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="24423-106">Arguments</span></span>

<span data-ttu-id="24423-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="24423-107">`text`: *String*</span></span>

<span data-ttu-id="24423-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="24423-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="24423-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="24423-109">Return values</span></span>

<span data-ttu-id="24423-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="24423-110">*String*</span></span>

<span data-ttu-id="24423-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="24423-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="24423-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="24423-112">Example</span></span>

<span data-ttu-id="24423-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` gibt **"Sample text"** zurück.</span><span class="sxs-lookup"><span data-stu-id="24423-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="24423-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="24423-114">Additional resources</span></span>

[<span data-ttu-id="24423-115">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="24423-115">Text functions</span></span>](er-functions-category-text.md)
