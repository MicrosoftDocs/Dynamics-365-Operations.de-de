---
title: SESSIONNOW EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SESSIONNOW-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 47b88a1ca0ea9fd09c2a82963901d9ace78891bb
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746793"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="56f34-103">SESSIONNOW EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="56f34-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="56f34-104">Die Funktion `SESSIONNOW` gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit der Anwendungssitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="56f34-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="56f34-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="56f34-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="56f34-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="56f34-106">Return values</span></span>

<span data-ttu-id="56f34-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="56f34-107">*DateTime*</span></span>

<span data-ttu-id="56f34-108">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="56f34-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="56f34-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="56f34-109">Example</span></span>

<span data-ttu-id="56f34-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` gibt das aktuelle Datum/den Zeitwert der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="56f34-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="56f34-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="56f34-111">Additional resources</span></span>

[<span data-ttu-id="56f34-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="56f34-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]