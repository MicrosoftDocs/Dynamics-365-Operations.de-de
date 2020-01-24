---
title: SESSIONTODAY EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der SESSIONTODAY-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: bcfb36d6e3fb8475546f7cfb420c4aca848ac896
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917464"
---
# <span data-ttu-id="e7f1a-103"><a name="SESSIONTODAY">SESSIONTODAY EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="e7f1a-103"><a name="SESSIONTODAY">SESSIONTODAY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e7f1a-104">Die Funktion `SESSIONTODAY` gibt den Wert *Date* zurück, der das aktuelle Anwendungssitzungsdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="e7f1a-104">The `SESSIONTODAY` function returns a *Date* value that represents the current application session date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7f1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e7f1a-105">Syntax</span></span>

```
SESSIONTODAY ()
```

## <a name="return-values"></a><span data-ttu-id="e7f1a-106">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e7f1a-106">Return values</span></span>

<span data-ttu-id="e7f1a-107">*Datum*</span><span class="sxs-lookup"><span data-stu-id="e7f1a-107">*Date*</span></span>

<span data-ttu-id="e7f1a-108">Der resultierende Datenwert.</span><span class="sxs-lookup"><span data-stu-id="e7f1a-108">The resulting date value.</span></span>

## <a name="example"></a><span data-ttu-id="e7f1a-109">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e7f1a-109">Example</span></span>

<span data-ttu-id="e7f1a-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` gibt das aktuelle Datum der Anwendungssitzung, den 24. Dezember 2015, als Zeichenfolge **"24-12-2015"** basierend auf den ausgewählten kulturspezifischen Kriterien für Deutschland und dem angegebenen Format zurück.</span><span class="sxs-lookup"><span data-stu-id="e7f1a-110">`DATEFORMAT (SESSIONTODAY (), "d", "DE")` returns the current application session date, December 24, 2015, as the string **"24-12-2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7f1a-111">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e7f1a-111">Additional resources</span></span>

[<span data-ttu-id="e7f1a-112">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="e7f1a-112">Date and time functions</span></span>](er-functions-category-datetime.md)
