---
title: SESSIONNOW EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SESSIONNOW-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: 4dff6daa8fbd60ef1fc84d783e428d69477aac6d
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916268"
---
# <span data-ttu-id="99c69-103"><a name="">SESSIONNOW EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="99c69-103"><a name="">SESSIONNOW ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99c69-104">Die Funktion `SESSIONNOW` gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit der Anwendungssitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="99c69-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="99c69-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="99c69-105">Syntax</span></span>

```
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="99c69-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="99c69-106">Return values</span></span>

<span data-ttu-id="99c69-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="99c69-107">*DateTime*</span></span>

<span data-ttu-id="99c69-108">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="99c69-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="99c69-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="99c69-109">Example</span></span>

<span data-ttu-id="99c69-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` gibt das aktuelle Datum/den Zeitwert der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="99c69-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="99c69-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="99c69-111">Additional resources</span></span>

[<span data-ttu-id="99c69-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="99c69-112">Date and time functions</span></span>](er-functions-category-datetime.md)