---
title: ADDDAYS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von ADDDAYS bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 85ad6508c0d16796efbf1ad81e25d74365de8f30
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570771"
---
# <a name="adddays-er-function"></a><span data-ttu-id="37dd5-103">ADDDAYS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="37dd5-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37dd5-104">Die Funktion `ADDDAYS` berechnet den Wert *DateTime*, der die angegebene Anzahl von Tagen vor oder nach einem angegebenen Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="37dd5-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="37dd5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="37dd5-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="37dd5-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="37dd5-106">Arguments</span></span>

<span data-ttu-id="37dd5-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="37dd5-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="37dd5-108">Ein Datums-/Zeitwert, der das Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="37dd5-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="37dd5-109">`days`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="37dd5-109">`days`: *Integer*</span></span>

<span data-ttu-id="37dd5-110">Die Anzahl von Tagen vor oder nach `datetime`.</span><span class="sxs-lookup"><span data-stu-id="37dd5-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="37dd5-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="37dd5-111">Return values</span></span>

<span data-ttu-id="37dd5-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="37dd5-112">*DateTime*</span></span>

<span data-ttu-id="37dd5-113">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="37dd5-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="37dd5-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="37dd5-114">Usage notes</span></span>

<span data-ttu-id="37dd5-115">Ein positiver Wert für `days` ergibt ein zukünftiges Datum.</span><span class="sxs-lookup"><span data-stu-id="37dd5-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="37dd5-116">Ein negativer Wert ergibt ein vergangenes Datum.</span><span class="sxs-lookup"><span data-stu-id="37dd5-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="37dd5-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37dd5-117">Example 1</span></span>

<span data-ttu-id="37dd5-118">`ADDDAYS (NOW(), 7)` gibt das Datum und die Uhrzeit sieben Tage in der Zukunft zurück.</span><span class="sxs-lookup"><span data-stu-id="37dd5-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="37dd5-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="37dd5-119">Example 2</span></span>

<span data-ttu-id="37dd5-120">`ADDDAYS (NOW(), -3)` gibt das Datum und die Uhrzeit drei Tage in der Vergangenheit zurück.</span><span class="sxs-lookup"><span data-stu-id="37dd5-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37dd5-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="37dd5-121">Additional resources</span></span>

[<span data-ttu-id="37dd5-122">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="37dd5-122">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]