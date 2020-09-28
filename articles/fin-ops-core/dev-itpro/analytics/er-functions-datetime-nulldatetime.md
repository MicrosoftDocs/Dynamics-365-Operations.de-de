---
title: NULLDATETIME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von NULLDATETIME bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: 9e1aaed3e85fc99d6451577d19e834afd37ad008
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743542"
---
# <a name="nulldatetime-er-function"></a><span data-ttu-id="38b92-103">NULLDATETIME EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="38b92-103">NULLDATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38b92-104">Die Funktion `NULLDATETIME` gibt den Wert *DateTime* zurück, der den Wert für Datum/Uhrzeit **null** (01. Januar 1900) in Koordinierter Weltzeit (Greenwich Mean Time \[GMT\]) darstellt.</span><span class="sxs-lookup"><span data-stu-id="38b92-104">The `NULLDATETIME` function returns a *DateTime* value that represents the **null** date/time value (January 1, 1900) in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="38b92-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="38b92-105">Syntax</span></span>

```vb
NULLDATETIME ()
```

## <a name="return-values"></a><span data-ttu-id="38b92-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="38b92-106">Return values</span></span>

<span data-ttu-id="38b92-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="38b92-107">*DateTime*</span></span>

<span data-ttu-id="38b92-108">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="38b92-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="38b92-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="38b92-109">Example</span></span>

<span data-ttu-id="38b92-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` gibt den Zeichenkettenwert **1900-01-01T00:00:00.0000000+00:00** zurück, wenn er während eines Prozesses aufgerufen wird, der von einem Anwendungsbenutzer mit dem Zeitzonenwert **(GMT Koordinierte Weltzeit)** im Bereich **Sprach- und Länder-/Regionsvoreinstellungen** initiiert wird.</span><span class="sxs-lookup"><span data-stu-id="38b92-110">`DATETIMEFORMAT( NULLDATETIME(), "O")` returns the string value **1900-01-01T00:00:00.0000000+00:00** when it's called during a process that was initiated by an application user who has the time zone value **(GMT) Coordinated Universal Time** in the **Language and country/region preferences** section.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="38b92-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="38b92-111">Additional resources</span></span>

[<span data-ttu-id="38b92-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="38b92-112">Date and time functions</span></span>](er-functions-category-datetime.md)
