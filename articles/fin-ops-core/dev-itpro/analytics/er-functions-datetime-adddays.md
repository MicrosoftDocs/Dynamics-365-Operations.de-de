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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743374"
---
# <a name="adddays-er-function"></a><span data-ttu-id="17149-103">ADDDAYS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="17149-103">ADDDAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17149-104">Die Funktion `ADDDAYS` berechnet den Wert *DateTime*, der die angegebene Anzahl von Tagen vor oder nach einem angegebenen Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="17149-104">The `ADDDAYS` function calculates a *DateTime* value that is the specified number of days before or after a specified start date.</span></span>

## <a name="syntax"></a><span data-ttu-id="17149-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="17149-105">Syntax</span></span>

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a><span data-ttu-id="17149-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="17149-106">Arguments</span></span>

<span data-ttu-id="17149-107">`datetime`: *DateTime*</span><span class="sxs-lookup"><span data-stu-id="17149-107">`datetime`: *DateTime*</span></span>

<span data-ttu-id="17149-108">Ein Datums-/Zeitwert, der das Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="17149-108">A date/time value that represents the start date.</span></span>

<span data-ttu-id="17149-109">`days`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="17149-109">`days`: *Integer*</span></span>

<span data-ttu-id="17149-110">Die Anzahl von Tagen vor oder nach `datetime`.</span><span class="sxs-lookup"><span data-stu-id="17149-110">The number of days before or after `datetime`.</span></span>

## <a name="return-values"></a><span data-ttu-id="17149-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="17149-111">Return values</span></span>

<span data-ttu-id="17149-112">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="17149-112">*DateTime*</span></span>

<span data-ttu-id="17149-113">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="17149-113">The resulting date/time value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="17149-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="17149-114">Usage notes</span></span>

<span data-ttu-id="17149-115">Ein positiver Wert für `days` ergibt ein zukünftiges Datum.</span><span class="sxs-lookup"><span data-stu-id="17149-115">A positive value for `days` yields a future date.</span></span> <span data-ttu-id="17149-116">Ein negativer Wert ergibt ein vergangenes Datum.</span><span class="sxs-lookup"><span data-stu-id="17149-116">A negative value yields a past date.</span></span>

## <a name="example-1"></a><span data-ttu-id="17149-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="17149-117">Example 1</span></span>

<span data-ttu-id="17149-118">`ADDDAYS (NOW(), 7)` gibt das Datum und die Uhrzeit sieben Tage in der Zukunft zurück.</span><span class="sxs-lookup"><span data-stu-id="17149-118">`ADDDAYS (NOW(), 7)` returns the date and time seven days in the future.</span></span>

## <a name="example-2"></a><span data-ttu-id="17149-119">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="17149-119">Example 2</span></span>

<span data-ttu-id="17149-120">`ADDDAYS (NOW(), -3)` gibt das Datum und die Uhrzeit drei Tage in der Vergangenheit zurück.</span><span class="sxs-lookup"><span data-stu-id="17149-120">`ADDDAYS (NOW(), -3)` returns the date and time three days in the past.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="17149-121">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="17149-121">Additional resources</span></span>

[<span data-ttu-id="17149-122">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="17149-122">Date and time functions</span></span>](er-functions-category-datetime.md)
