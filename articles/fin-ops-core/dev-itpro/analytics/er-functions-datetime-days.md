---
title: DAYS EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DAYS bei der elektronischen Berichterstellungsfunktion (EB) bereitgestellt.
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
ms.openlocfilehash: 66398e624e4b9d69d4dc3ccf3ee8f97758f4f861
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682340"
---
# <a name="days-er-function"></a><span data-ttu-id="aa109-103">DAYS EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="aa109-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aa109-104">Die Funktion `DAYS` gibt einen Wert für *Integer* zurück, der die Anzahl der Tage zwischen einem angegebenen Datum und einem zweiten angegebenen Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa109-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa109-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aa109-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="aa109-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="aa109-106">Arguments</span></span>

<span data-ttu-id="aa109-107">`date 1`: *Date*</span><span class="sxs-lookup"><span data-stu-id="aa109-107">`date 1`: *Date*</span></span>

<span data-ttu-id="aa109-108">Ein Datumswert, der das für die Berechnung der Anzahl der Tage zu verwendende Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa109-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="aa109-109">`date 2`: *Date*</span><span class="sxs-lookup"><span data-stu-id="aa109-109">`date 2`: *Date*</span></span>

<span data-ttu-id="aa109-110">Ein Datumswert, der das für die Berechnung der Anzahl der Tage zu verwendende Enddatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="aa109-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="aa109-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="aa109-111">Return values</span></span>

<span data-ttu-id="aa109-112">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="aa109-112">*Integer*</span></span>

<span data-ttu-id="aa109-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="aa109-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="aa109-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="aa109-114">Usage notes</span></span>

<span data-ttu-id="aa109-115">Die Funktion `DAYS` gibt einen positiven Wert zurück, wenn das erste Datum nach dem zweiten Datum liegt. Sie gibt **0** (null) zurück, wenn das erste Datum gleich dem zweiten Datum ist, oder sie gibt einen negativen Wert zurück, wenn das erste Datum vor dem zweiten Datum liegt.</span><span class="sxs-lookup"><span data-stu-id="aa109-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="aa109-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="aa109-116">Example</span></span>

<span data-ttu-id="aa109-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` gibt **-1** zurück.</span><span class="sxs-lookup"><span data-stu-id="aa109-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="aa109-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="aa109-118">Additional resources</span></span>

[<span data-ttu-id="aa109-119">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="aa109-119">Date and time functions</span></span>](er-functions-category-datetime.md)
