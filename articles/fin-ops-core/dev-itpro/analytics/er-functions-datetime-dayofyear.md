---
title: DAYOFYEAR EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der DAYOFYEAR-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d24aabb582151b0b357b64a988cc932a9c9f3cea
ms.sourcegitcommit: 3dede95a3b17de920bb0adcb33029f990682752b
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/18/2020
ms.locfileid: "3070666"
---
# <span data-ttu-id="cb01d-103"><a name="DAYOFYEAR">DAYOFYEAR EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="cb01d-103"><a name="DAYOFYEAR">DAYOFYEAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cb01d-104">Die Funktion `DAYOFYEAR` gibt einen Wert für *Integer* zurück, der die Anzahl der Tage zwischen dem 01. Januar und dem angegebenen Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="cb01d-104">The `DAYOFYEAR` function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb01d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb01d-105">Syntax</span></span>

```vb
DAYOFYEAR (date) as Integer
```

## <a name="arguments"></a><span data-ttu-id="cb01d-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="cb01d-106">Arguments</span></span>

<span data-ttu-id="cb01d-107">`date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="cb01d-107">`date`: *Date*</span></span>

<span data-ttu-id="cb01d-108">Ein Datumswert, der das für die Berechnung der Anzahl der Tage zu verwendende Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="cb01d-108">A date value that represents the date to use for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="cb01d-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="cb01d-109">Return values</span></span>

<span data-ttu-id="cb01d-110">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="cb01d-110">*Integer*</span></span>

<span data-ttu-id="cb01d-111">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="cb01d-111">The resulting numeric value.</span></span>

## <a name="example-1"></a><span data-ttu-id="cb01d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cb01d-112">Example 1</span></span>

<span data-ttu-id="cb01d-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` gibt **61** zurück.</span><span class="sxs-lookup"><span data-stu-id="cb01d-113">`DAYOFYEAR (DATEVALUE ("01-03-2016", "dd-MM-yyyy"))` returns **61**.</span></span>

## <a name="example-2"></a><span data-ttu-id="cb01d-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="cb01d-114">Example 2</span></span>

<span data-ttu-id="cb01d-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` gibt **1** zurück.</span><span class="sxs-lookup"><span data-stu-id="cb01d-115">`DAYOFYEAR (DATEVALUE ("01-01-2016", "dd-MM-yyyy"))` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cb01d-116">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="cb01d-116">Additional resources</span></span>

[<span data-ttu-id="cb01d-117">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="cb01d-117">Date and time functions</span></span>](er-functions-category-datetime.md)
