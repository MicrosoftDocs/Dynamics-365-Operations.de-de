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
ms.openlocfilehash: 77854d645ba5b65a2819437af510fcd67be6d99d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040939"
---
# <span data-ttu-id="fc74b-103"><a name="UPPER">UPPER EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="fc74b-103"><a name="UPPER">UPPER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc74b-104">Die Funktion `UPPER` gibt die angegebene Textzeichenfolge mit dem Wert *String* zurück, nachdem er in Großbuchstaben umgewandelt wurde.</span><span class="sxs-lookup"><span data-stu-id="fc74b-104">The `UPPER` function returns the specified text string as a *String* value after it has been converted to uppercase letters.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc74b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc74b-105">Syntax</span></span>

```vb
UPPER (text )
```

## <a name="arguments"></a><span data-ttu-id="fc74b-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="fc74b-106">Arguments</span></span>

<span data-ttu-id="fc74b-107">`text`: *String*</span><span class="sxs-lookup"><span data-stu-id="fc74b-107">`text`: *String*</span></span>

<span data-ttu-id="fc74b-108">Der gültige Pfad einer Datenquelle des Typs *String*.</span><span class="sxs-lookup"><span data-stu-id="fc74b-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fc74b-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="fc74b-109">Return values</span></span>

<span data-ttu-id="fc74b-110">*Zeichenfolge*</span><span class="sxs-lookup"><span data-stu-id="fc74b-110">*String*</span></span>

<span data-ttu-id="fc74b-111">Der resultierende Textwert.</span><span class="sxs-lookup"><span data-stu-id="fc74b-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="fc74b-112">Beispiel</span><span class="sxs-lookup"><span data-stu-id="fc74b-112">Example</span></span>

<span data-ttu-id="fc74b-113">`UPPER ("Sample")` gibt **"SAMPLE"** zurück.</span><span class="sxs-lookup"><span data-stu-id="fc74b-113">`UPPER ("Sample")` returns **"SAMPLE"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="fc74b-114">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="fc74b-114">Additional resources</span></span>

[<span data-ttu-id="fc74b-115">Textfunktionen</span><span class="sxs-lookup"><span data-stu-id="fc74b-115">Text functions</span></span>](er-functions-category-text.md)
