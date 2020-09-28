---
title: TODAY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von TODAY bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: e2ee153c1dde99810a78ed15c7505fa705088797
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745440"
---
# <a name="today-er-function"></a><span data-ttu-id="e24ca-103">TODAY EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="e24ca-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e24ca-104">Diese Funktion `TODAY` gibt den Wert *Date* zurück, der das aktuelle Anwendungsserverdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="e24ca-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e24ca-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e24ca-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e24ca-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e24ca-106">Return values</span></span>

<span data-ttu-id="e24ca-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="e24ca-107">*Date*</span></span>

<span data-ttu-id="e24ca-108">Der resultierende Datenwert.</span><span class="sxs-lookup"><span data-stu-id="e24ca-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e24ca-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e24ca-109">Example</span></span>

<span data-ttu-id="e24ca-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format als Zeichenfolge **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="e24ca-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e24ca-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e24ca-111">Additional resources</span></span>

[<span data-ttu-id="e24ca-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="e24ca-112">Date and time functions</span></span>](er-functions-category-datetime.md)
