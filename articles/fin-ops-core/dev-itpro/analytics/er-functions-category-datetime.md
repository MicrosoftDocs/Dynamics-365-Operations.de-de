---
title: Liste der EB-Funktionen in der Kategorie „Datum und Uhrzeit“
description: Dieses Thema enthält Informationen zu den Datums- und Uhrzeitfunktionen, die in der elektronischen Berichterstellung (EB) unterstützt werden.
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
ms.openlocfilehash: fa8e725ac6bd7d280dc0269a70e3f7abf1ad4d43
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916567"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a><span data-ttu-id="14ba3-103">Liste der EB-Funktionen in der Kategorie „Datum und Uhrzeit“</span><span class="sxs-lookup"><span data-stu-id="14ba3-103">List of ER functions in the Date and time category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="14ba3-104">Datums- und Zeitfunktionen für die elektronische Berichterstellung (EB) können verwendet werden, um Informationen aus Datums- und Zeitwerten zu extrahieren und Operationen an diesen durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="14ba3-104">Electronic reporting (ER) date and time functions can be used to extract information from date and time values, and to perform operations on them.</span></span> <span data-ttu-id="14ba3-105">Dieses Thema enthält eine Zusammenfassung dieser Funktionen.</span><span class="sxs-lookup"><span data-stu-id="14ba3-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="14ba3-106">Liste der unterstützten Funktionen</span><span class="sxs-lookup"><span data-stu-id="14ba3-106">List of supported functions</span></span>

| <span data-ttu-id="14ba3-107">Funktion</span><span class="sxs-lookup"><span data-stu-id="14ba3-107">Function</span></span> | <span data-ttu-id="14ba3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="14ba3-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="14ba3-109">AddDays</span><span class="sxs-lookup"><span data-stu-id="14ba3-109">AddDays</span></span>](er-functions-datetime-adddays.md) | <span data-ttu-id="14ba3-110">Diese Funktion gibt den Wert *DateTime* zurück, der die angegebene Anzahl von Tagen vor oder nach einem angegebenen Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-110">This function returns a *DateTime* value that is the specified number of days before or after a specified start date.</span></span> |
| [<span data-ttu-id="14ba3-111">DateFormat</span><span class="sxs-lookup"><span data-stu-id="14ba3-111">DateFormat</span></span>](er-functions-datetime-dateformat.md) | <span data-ttu-id="14ba3-112">Diese Funktion gibt den Wert *String* zurück, der einen vorgegebenen Datenwert als Text im angegebenen Format und in einer optional angegebenen Kultur darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-112">This function returns a *String* value that presents a given date value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="14ba3-113">DateTimeFormat</span><span class="sxs-lookup"><span data-stu-id="14ba3-113">DateTimeFormat</span></span>](er-functions-datetime-datetimeformat.md) | <span data-ttu-id="14ba3-114">Diese Funktion gibt den Wert *String* zurück, der einen vorgegebenen Wert für Datum/Uhrzeit als Text im angegebenen Format und in einer optional angegebenen Kultur darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-114">This function returns a *String* value that presents a given date/time value as text in the specified format and in an optionally specified culture.</span></span> |
| [<span data-ttu-id="14ba3-115">DateTimeValue</span><span class="sxs-lookup"><span data-stu-id="14ba3-115">DateTimeValue</span></span>](er-functions-datetime-datetimevalue.md) | <span data-ttu-id="14ba3-116">Diese Funktion gibt den Wert *DateTime* zurück, der über einen vorgegebenen Textwert in das spezielle Format und in einen optional angegebenen Wert für Datum/Uhrzeit konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="14ba3-116">This function returns a *DateTime* value that is converted from a given text value in the specified format and in an optionally specified culture to a date/time value.</span></span> |
| [<span data-ttu-id="14ba3-117">DateToDateTime</span><span class="sxs-lookup"><span data-stu-id="14ba3-117">DateToDateTime</span></span>](er-functions-datetime-datetodatetime.md) | <span data-ttu-id="14ba3-118">Diese Funktion gibt den Wert *DateTime* zurück, der über einen vorgegebenen Datumswert in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="14ba3-118">This function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span> |
| [<span data-ttu-id="14ba3-119">DateValue</span><span class="sxs-lookup"><span data-stu-id="14ba3-119">DateValue</span></span>](er-functions-datetime-datevalue.md) | <span data-ttu-id="14ba3-120">Diese Funktion gibt den Wert *Date* zurück, der über einen vorgegebenen Textwert in das spezielle Format und in einen optional angegebenen Wert für Datum/Uhrzeit konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="14ba3-120">This function returns a *Date* value that is converted from a given text value in the specified format and in an optionally specified culture to a date value.</span></span> |
| [<span data-ttu-id="14ba3-121">DayOfYear</span><span class="sxs-lookup"><span data-stu-id="14ba3-121">DayOfYear</span></span>](er-functions-datetime-dayofyear.md) | <span data-ttu-id="14ba3-122">Diese Funktion gibt einen Wert für *Ganzzahl* zurück, der die Anzahl der Tage zwischen dem 01. Januar und dem angegebenen Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-122">This function returns an *Integer* value that represents the number of days between January 1 and the specified date.</span></span> |
| [<span data-ttu-id="14ba3-123">Tage</span><span class="sxs-lookup"><span data-stu-id="14ba3-123">Days</span></span>](er-functions-datetime-days.md) | <span data-ttu-id="14ba3-124">Diese Funktion gibt einen Wert für *Ganzzahl* zurück, der die Anzahl der Tage zwischen einem angegebenen Datum und einem zweiten angegebenen Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-124">This function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span> |
| [<span data-ttu-id="14ba3-125">Now</span><span class="sxs-lookup"><span data-stu-id="14ba3-125">Now</span></span>](er-functions-datetime-now.md) | <span data-ttu-id="14ba3-126">Diese Funktion gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit des Anwendungsservers darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-126">This function returns a *DateTime* value that represents the current application server date and time.</span></span> |
| [<span data-ttu-id="14ba3-127">NullDate</span><span class="sxs-lookup"><span data-stu-id="14ba3-127">NullDate</span></span>](er-functions-datetime-nulldate.md) | <span data-ttu-id="14ba3-128">Diese Funktion gibt den Wert *Date* zurück, der das Datum **null** (01. Januar 1900) darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-128">This function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span> |
| [<span data-ttu-id="14ba3-129">NullDateTime</span><span class="sxs-lookup"><span data-stu-id="14ba3-129">NullDateTime</span></span>](er-functions-datetime-nulldatetime.md) | <span data-ttu-id="14ba3-130">Diese Funktion gibt den Wert *DateTime* zurück, der den Wert für Datum/Uhrzeit **null** (01. Januar 1900) in Koordinierter Weltzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-130">This function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time.</span></span> |
| [<span data-ttu-id="14ba3-131">SessionNow</span><span class="sxs-lookup"><span data-stu-id="14ba3-131">SessionNow</span></span>](er-functions-datetime-sessionnow.md) | <span data-ttu-id="14ba3-132">Diese Funktion gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit der Anwendungssitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-132">This function returns a *DateTime* value that represents the current application session date and time.</span></span> |
| [<span data-ttu-id="14ba3-133">SessionToday</span><span class="sxs-lookup"><span data-stu-id="14ba3-133">SessionToday</span></span>](er-functions-datetime-sessiontoday.md) | <span data-ttu-id="14ba3-134">Diese Funktion gibt den Wert *Date* zurück, der das aktuelle Anwendungssitzungsdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-134">This function returns a *Date* value that represents the current application session date.</span></span> |
| [<span data-ttu-id="14ba3-135">Heute</span><span class="sxs-lookup"><span data-stu-id="14ba3-135">Today</span></span>](er-functions-datetime-today.md) | <span data-ttu-id="14ba3-136">Diese Funktion gibt den Wert *Date* zurück, der das aktuelle Anwendungsserverdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="14ba3-136">This function returns a *Date* value that represents the current application server date.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="14ba3-137">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="14ba3-137">Additional resources</span></span>

[<span data-ttu-id="14ba3-138">Überblick über die elektronische Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="14ba3-138">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="14ba3-139">Formeldesigner in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="14ba3-139">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="14ba3-140">Formelsprache in der elektronischen Berichterstellung</span><span class="sxs-lookup"><span data-stu-id="14ba3-140">Electronic reporting formula language</span></span>](er-formula-language.md)
