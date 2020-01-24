---
title: DATETODATETIME EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung von DATETODATETIME bei der elektronischen Berichterstellung (EB) bereitgestellt.
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
ms.openlocfilehash: f9ce977b36cd96a27a228dba1bc8c8445bafd879
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916383"
---
# <span data-ttu-id="d670c-103"><a name="DATETODATETIME">DATETODATETIME EB-Funktion</a></span><span class="sxs-lookup"><span data-stu-id="d670c-103"><a name="DATETODATETIME">DATETODATETIME ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d670c-104">Die Funktion `DATETODATETIME` gibt den Wert *DateTime* zurück, der über den vorgegebenen Datumswert in einen Wert für Datum/Uhrzeit in der Koordinierten Weltzeit (Greenwich Mean Time \[GMT\]) konvertiert wird.</span><span class="sxs-lookup"><span data-stu-id="d670c-104">The `DATETODATETIME` function returns a *DateTime* value that is converted from a given date value to a date/time value in Coordinated Universal Time (Greenwich Mean Time \[GMT\]).</span></span>

## <a name="syntax"></a><span data-ttu-id="d670c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d670c-105">Syntax</span></span>

```
DATETODATETIME (date)
```

## <a name="arguments"></a><span data-ttu-id="d670c-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="d670c-106">Arguments</span></span>

<span data-ttu-id="d670c-107">`date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="d670c-107">`date`: *Date*</span></span>

<span data-ttu-id="d670c-108">Ein Datumswert, der das zu konvertierende Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="d670c-108">A date value that represents the date to convert.</span></span>

## <a name="return-values"></a><span data-ttu-id="d670c-109">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="d670c-109">Return values</span></span>

<span data-ttu-id="d670c-110">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="d670c-110">*DateTime*</span></span>

<span data-ttu-id="d670c-111">Der resultierende Wert für Datum/Uhrzeit.</span><span class="sxs-lookup"><span data-stu-id="d670c-111">The resulting date/time value.</span></span>

## <a name="example-1"></a><span data-ttu-id="d670c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d670c-112">Example 1</span></span>

<span data-ttu-id="d670c-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` gibt das Datum der aktuellen Microsoft Dynamics 365 Finance-Sitzung, Dezember 24, 2015, mit **12/24/2015 12:00:00 AM** zurück.</span><span class="sxs-lookup"><span data-stu-id="d670c-113">`DATETODATETIME (CompInfo. 'getCurrentDate()')` returns the date of the current Microsoft Dynamics 365 Finance session, December 24, 2015, as **12/24/2015 12:00:00 AM**.</span></span> <span data-ttu-id="d670c-114">In diesem Beispiel ist **CompInfo** eine Datenquelle der elektronischen Berichterstellung (EB) des Typs **Finance and Operations/Tabelle** und bezieht sich auf die Tabelle „CompanyInfo“.</span><span class="sxs-lookup"><span data-stu-id="d670c-114">In this example, **CompInfo** is an Electronic reporting (ER) data source of the **Finance and Operations/Table** type, and it refers to the CompanyInfo table.</span></span>

## <a name="example-2"></a><span data-ttu-id="d670c-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d670c-115">Example 2</span></span>

<span data-ttu-id="d670c-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` gibt den Wert **11/12/2019 12:00:00 AM** für Datum/Uhrzeit zurück.</span><span class="sxs-lookup"><span data-stu-id="d670c-116">`DATETODATETIME (DATEVALUE ("2019-11-12T16:00:00.0000000-07:00", "O"))` returns the date/time value **11/12/2019 12:00:00 AM**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d670c-117">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d670c-117">Additional resources</span></span>

[<span data-ttu-id="d670c-118">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="d670c-118">Date and time functions</span></span>](er-functions-category-datetime.md)
