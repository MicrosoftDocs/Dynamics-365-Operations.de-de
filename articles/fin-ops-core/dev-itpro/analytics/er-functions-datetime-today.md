---
title: TODAY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von TODAY bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
author: NickSelin
ms.date: 12/05/2019
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
ms.openlocfilehash: 45ee4282acf4d6a5febe4b74b6955410e73e86a3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746746"
---
# <a name="today-er-function"></a><span data-ttu-id="4638b-103">TODAY EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="4638b-103">TODAY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4638b-104">Diese Funktion `TODAY` gibt den Wert *Date* zurück, der das aktuelle Anwendungsserverdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="4638b-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="4638b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="4638b-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="4638b-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="4638b-106">Return values</span></span>

<span data-ttu-id="4638b-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="4638b-107">*Date*</span></span>

<span data-ttu-id="4638b-108">Der resultierende Datenwert.</span><span class="sxs-lookup"><span data-stu-id="4638b-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="4638b-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="4638b-109">Example</span></span>

<span data-ttu-id="4638b-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format als Zeichenfolge **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="4638b-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4638b-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="4638b-111">Additional resources</span></span>

[<span data-ttu-id="4638b-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="4638b-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]