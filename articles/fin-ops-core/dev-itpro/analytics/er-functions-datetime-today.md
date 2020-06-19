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
ms.openlocfilehash: 94ef15d1971287e8bf13944bc8f693b567950031
ms.sourcegitcommit: b52477b7d0d52102a7ca2fb95f4ebfa30ecd9f54
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2020
ms.locfileid: "3411436"
---
# <a name=""></a><span data-ttu-id="b2e66-103"><a name="TODAY">TODAY EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="b2e66-103"><a name="TODAY">TODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b2e66-104">Diese Funktion `TODAY` gibt den Wert *Date* zurück, der das aktuelle Anwendungsserverdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="b2e66-104">The `TODAY` function returns a *Date* value that represents the current application server date.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2e66-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b2e66-105">Syntax</span></span>

```xpp
TODAY ()
```

## <a name="return-values"></a><span data-ttu-id="b2e66-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="b2e66-106">Return values</span></span>

<span data-ttu-id="b2e66-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="b2e66-107">*Date*</span></span>

<span data-ttu-id="b2e66-108">Der resultierende Datenwert.</span><span class="sxs-lookup"><span data-stu-id="b2e66-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="b2e66-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="b2e66-109">Example</span></span>

<span data-ttu-id="b2e66-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` gibt den Wert für das aktuelle Datum des Anwendungsservers, 24. Dezember 2015, basierend auf dem angegebenen benutzerdefinierten Format als Zeichenfolge **"24-12-2015"** zurück.</span><span class="sxs-lookup"><span data-stu-id="b2e66-110">`DATEFORMAT (TODAY (), "dd-MM-yyyy")` returns the current application server date, December 24, 2015, as the string **"24-12-2015"**, based on the specified custom format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b2e66-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="b2e66-111">Additional resources</span></span>

[<span data-ttu-id="b2e66-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="b2e66-112">Date and time functions</span></span>](er-functions-category-datetime.md)
