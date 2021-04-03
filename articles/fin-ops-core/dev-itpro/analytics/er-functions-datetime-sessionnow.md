---
title: SESSIONNOW EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SESSIONNOW-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: a79e8055a4b5025e1b1c4ab91875cf165fa8b354
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563390"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="28af8-103">SESSIONNOW EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="28af8-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28af8-104">Die Funktion `SESSIONNOW` gibt den Wert *DateTime* zurück, der das aktuelle Datum und die Uhrzeit der Anwendungssitzung darstellt.</span><span class="sxs-lookup"><span data-stu-id="28af8-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="28af8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="28af8-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="28af8-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="28af8-106">Return values</span></span>

<span data-ttu-id="28af8-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="28af8-107">*DateTime*</span></span>

<span data-ttu-id="28af8-108">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="28af8-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="28af8-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="28af8-109">Example</span></span>

<span data-ttu-id="28af8-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` gibt das aktuelle Datum/den Zeitwert der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="28af8-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28af8-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="28af8-111">Additional resources</span></span>

[<span data-ttu-id="28af8-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="28af8-112">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]