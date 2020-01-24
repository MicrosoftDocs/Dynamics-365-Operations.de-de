---
title: ADDDAYS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von ADDDAYS bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: dd1290538c506cd0db6eb21a304ff9812c808f17
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916452"
---
# <span data-ttu-id="0eb0e-103"><a name="ADDDAYS">ADDDAYS EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="0eb0e-103"><a name="ADDDAYS">ADDDAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0eb0e-104">Die Funktion `ADDDAYS` berechnet den Wert *DateTime*, der die angegebene Anzahl von Tagen vor oder nach einem angegebenen Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="0eb0e-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="0eb0e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0eb0e-105">Syntax</span></span>

```
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="0eb0e-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="0eb0e-106">Arguments</span></span>

<span data-ttu-id="0eb0e-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="0eb0e-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="0eb0e-108">Ein Datums-/Zeitwert, der das Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="0eb0e-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="0eb0e-109">`days`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="0eb0e-109">`days`: *Integer*</span></span>

<span data-ttu-id="0eb0e-110">Die Anzahl von Tagen vor oder nach `datetime`.</span><span class="sxs-lookup"><span data-stu-id="0eb0e-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="0eb0e-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0eb0e-111">Return values</span></span>

<span data-ttu-id="0eb0e-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="0eb0e-112">*DateTime*</span></span>

<span data-ttu-id="0eb0e-113">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="0eb0e-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="0eb0e-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="0eb0e-114">Usage notes</span></span>

<span data-ttu-id="0eb0e-115">Ein positiver Wert für `days` ergibt ein zukünftiges Datum.</span><span class="sxs-lookup"><span data-stu-id="0eb0e-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="0eb0e-116">Ein negativer Wert ergibt ein vergangenes Datum.</span><span class="sxs-lookup"><span data-stu-id="0eb0e-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="0eb0e-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0eb0e-117">Example 1</span></span>

<span data-ttu-id="0eb0e-118">`ADDDAYS (NOW(), 7)` gibt das Datum und die Uhrzeit sieben Tage in der Zukunft zurück.</span><span class="sxs-lookup"><span data-stu-id="0eb0e-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="0eb0e-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0eb0e-119">Example 2</span></span>

<span data-ttu-id="0eb0e-120">`ADDDAYS (NOW(), -3)` gibt das Datum und die Uhrzeit drei Tage in der Vergangenheit zurück.</span><span class="sxs-lookup"><span data-stu-id="0eb0e-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0eb0e-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0eb0e-121">Additional resources</span></span>

[<span data-ttu-id="0eb0e-122">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="0eb0e-122">Date and time functions</span></span>](er-functions-category-datetime.md)
