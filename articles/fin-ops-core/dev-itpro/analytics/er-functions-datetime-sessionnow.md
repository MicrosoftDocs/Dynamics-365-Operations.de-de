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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d70acb06194a28af0cc85eea440e9e4e937bc3bb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683842"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="ffeb9-103">SESSIONNOW EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="ffeb9-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ffeb9-104">Die Funktion `SESSIONNOW` gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit der Anwendungssitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ffeb9-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffeb9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ffeb9-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="ffeb9-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ffeb9-106">Return values</span></span>

<span data-ttu-id="ffeb9-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="ffeb9-107">*DateTime*</span></span>

<span data-ttu-id="ffeb9-108">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="ffeb9-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="ffeb9-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="ffeb9-109">Example</span></span>

<span data-ttu-id="ffeb9-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` gibt das aktuelle Datum/den Zeitwert der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="ffeb9-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffeb9-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ffeb9-111">Additional resources</span></span>

[<span data-ttu-id="ffeb9-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="ffeb9-112">Date and time functions</span></span>](er-functions-category-datetime.md)
