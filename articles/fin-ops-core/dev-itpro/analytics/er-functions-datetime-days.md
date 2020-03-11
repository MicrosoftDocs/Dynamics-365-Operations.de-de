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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62e34628712066d92a244676123ce928a468ea9e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042388"
---
# <span data-ttu-id="be1dd-103"><a name="DAYS">DAYS ER Funktion</a></span><span class="sxs-lookup"><span data-stu-id="be1dd-103"><a name="DAYS">DAYS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="be1dd-104">Die Funktion `DAYS` gibt einen Wert für *Integer* zurück, der die Anzahl der Tage zwischen einem angegebenen Datum und einem zweiten angegebenen Datum darstellt.</span><span class="sxs-lookup"><span data-stu-id="be1dd-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="be1dd-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="be1dd-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="be1dd-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="be1dd-106">Arguments</span></span>

<span data-ttu-id="be1dd-107">`date 1`: *Date*</span><span class="sxs-lookup"><span data-stu-id="be1dd-107">`date 1`: *Date*</span></span>

<span data-ttu-id="be1dd-108">Ein Datumswert, der das für die Berechnung der Anzahl der Tage zu verwendende Startdatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="be1dd-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="be1dd-109">`date 2`: *Date*</span><span class="sxs-lookup"><span data-stu-id="be1dd-109">`date 2`: *Date*</span></span>

<span data-ttu-id="be1dd-110">Ein Datumswert, der das für die Berechnung der Anzahl der Tage zu verwendende Enddatum darstellt.</span><span class="sxs-lookup"><span data-stu-id="be1dd-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="be1dd-111">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="be1dd-111">Return values</span></span>

<span data-ttu-id="be1dd-112">*Ganze Zahl*</span><span class="sxs-lookup"><span data-stu-id="be1dd-112">*Integer*</span></span>

<span data-ttu-id="be1dd-113">Der resultierende numerische Wert.</span><span class="sxs-lookup"><span data-stu-id="be1dd-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="be1dd-114">Anwendungshinweise</span><span class="sxs-lookup"><span data-stu-id="be1dd-114">Usage notes</span></span>

<span data-ttu-id="be1dd-115">Die Funktion `DAYS` gibt einen positiven Wert zurück, wenn das erste Datum nach dem zweiten Datum liegt. Sie gibt **0** (null) zurück, wenn das erste Datum gleich dem zweiten Datum ist, oder sie gibt einen negativen Wert zurück, wenn das erste Datum vor dem zweiten Datum liegt.</span><span class="sxs-lookup"><span data-stu-id="be1dd-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="be1dd-116">Beispiel</span><span class="sxs-lookup"><span data-stu-id="be1dd-116">Example</span></span>

<span data-ttu-id="be1dd-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` gibt **-1** zurück.</span><span class="sxs-lookup"><span data-stu-id="be1dd-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="be1dd-118">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="be1dd-118">Additional resources</span></span>

[<span data-ttu-id="be1dd-119">Datums- und Zeitfunktionen</span><span class="sxs-lookup"><span data-stu-id="be1dd-119">Date and time functions</span></span>](er-functions-category-datetime.md)
