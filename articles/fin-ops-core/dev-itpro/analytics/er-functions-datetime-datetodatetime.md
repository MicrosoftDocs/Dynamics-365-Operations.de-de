---
title: DATETODATETIME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETODATETIME bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: bb90c58544eeba804cd39542cc70fab3b840af80
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746962"
---
# <a name="datetodatetime-er-function"></a><span data-ttu-id="0345d-103">DATETODATETIME EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="0345d-103">DATETODATETIME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0345d-104">Die Funktion `DATETODATETIME` gibt den Wert *DateTime* zurück, der über den vorgegebenen Datumswert in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="0345d-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="0345d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0345d-105">Syntax</span></span>

```vb
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="0345d-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="0345d-106">Arguments</span></span>

<span data-ttu-id="0345d-107">`date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="0345d-107">`date`: *Date*</span></span>

<span data-ttu-id="0345d-108">Ein Datumswert, der das zu konvertierende Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="0345d-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="0345d-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="0345d-109">Return values</span></span>

<span data-ttu-id="0345d-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="0345d-110">*DateTime*</span></span>

<span data-ttu-id="0345d-111">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="0345d-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0345d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="0345d-112">Example 1</span></span>

<span data-ttu-id="0345d-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` gibt das Datum der aktuellen Microsoft Dynamics 365 Finance-Sitzung, Dezember 24, 2015, mit **12/24/2015 12:00:00 AM** zurück.</span><span class="sxs-lookup"><span data-stu-id="0345d-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="0345d-114">In diesem Beispiel ist **CompInfo** eine Datenquelle für die elektronische Berichterstattung (ER) vom Typ **Finance and Operations/Tabelle**, und sie bezieht sich auf die Tabelle CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="0345d-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="0345d-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="0345d-115">Example 2</span></span>

<span data-ttu-id="0345d-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` gibt den Wert **11/12/2019 12:00:00 AM** für Datum/Uhrzeit zurück.</span><span class="sxs-lookup"><span data-stu-id="0345d-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0345d-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="0345d-117">Additional resources</span></span>

[<span data-ttu-id="0345d-118">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="0345d-118">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]