---
title: NOW EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von NOW bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: e8c411e1ce9656ffa35986f1ceef712c9def1e6b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743518"
---
# <a name="now-er-function"></a><span data-ttu-id="82868-103">NOW EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="82868-103">NOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="82868-104">Die Funktion `NOW` gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit des Anwendungsservers darstellt.</span><span class="sxs-lookup"><span data-stu-id="82868-104">The `NOW` function returns a *DateTime* value that represents the current application server date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="82868-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="82868-105">Syntax</span></span>

```vb
NOW ()
```

## <a name="return-values"></a><span data-ttu-id="82868-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="82868-106">Return values</span></span>

<span data-ttu-id="82868-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="82868-107">*DateTime*</span></span>

<span data-ttu-id="82868-108">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="82868-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="82868-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="82868-109">Example</span></span>

<span data-ttu-id="82868-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum/die Uhrzeit des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format mit **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="82868-110">`DATETIMEFORMAT (NOW(), "dd-MM-yyyy")` returns the current application server date/time value, December 24, 2015, as **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="82868-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="82868-111">Additional resources</span></span>

[<span data-ttu-id="82868-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="82868-112">Date and time functions</span></span>](er-functions-category-datetime.md)
