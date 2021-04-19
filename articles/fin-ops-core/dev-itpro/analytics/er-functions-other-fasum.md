---
title: FA_SUM EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der FA_SUM-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744294"
---
# <a name="fa_sum-er-function"></a><span data-ttu-id="e89fc-103">FA_SUM EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="e89fc-103">FA_SUM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e89fc-104">Die Funktion `FA_SUM` gibt den Wert *Container (Datensatz)* zurück, der aus Daten für die Anlagenbeträge für die angegebene Anlagenposition, dem Wertmodellcode und den Datumszeiträumen besteht.</span><span class="sxs-lookup"><span data-stu-id="e89fc-104">The `FA_SUM` function returns a *Container (record)* value that consists of data for the fixed asset amounts for the specified fixed asset item, value model code, and period of dates.</span></span>

## <a name="syntax"></a><span data-ttu-id="e89fc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e89fc-105">Syntax</span></span>

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a><span data-ttu-id="e89fc-106">Argumente</span><span class="sxs-lookup"><span data-stu-id="e89fc-106">Arguments</span></span>

<span data-ttu-id="e89fc-107">`fixed asset code`: *String*</span><span class="sxs-lookup"><span data-stu-id="e89fc-107">`fixed asset code`: *String*</span></span>

<span data-ttu-id="e89fc-108">Der Wert *String*, der den Code eines Gegenstands des Anlagevermögens darstellt, für den der Saldo berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e89fc-108">A *String* value that represents the code of a fixed asset item that the balance is calculated for.</span></span>

<span data-ttu-id="e89fc-109">`value model code`: *String*</span><span class="sxs-lookup"><span data-stu-id="e89fc-109">`value model code`: *String*</span></span>

<span data-ttu-id="e89fc-110">Der Wert *String*, der den Code eines Gegenstands des Wertmodells darstellt, für das der Saldo berechnet wird.</span><span class="sxs-lookup"><span data-stu-id="e89fc-110">A *String* value that represents the code of a value model that the balance is calculated for.</span></span>

<span data-ttu-id="e89fc-111">`start date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="e89fc-111">`start date`: *Date*</span></span>

<span data-ttu-id="e89fc-112">Ein Wert *Date*, der das Startdatum eines Zeitraums darstellt, für den die Beträge des Anlagevermögens berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="e89fc-112">A *Date* value that represents the start date of a period that the fixed asset amounts are calculated for.</span></span>

<span data-ttu-id="e89fc-113">`end date`: *Date*</span><span class="sxs-lookup"><span data-stu-id="e89fc-113">`end date`: *Date*</span></span>

<span data-ttu-id="e89fc-114">Ein Wert *Date*, der das Enddatum eines Zeitraums darstellt, für den die Beträge des Anlagevermögens berechnet werden.</span><span class="sxs-lookup"><span data-stu-id="e89fc-114">A *Date* value that represents the end date of a period that the fixed asset amounts are calculated for.</span></span>

## <a name="return-values"></a><span data-ttu-id="e89fc-115">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="e89fc-115">Return values</span></span>

<span data-ttu-id="e89fc-116">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="e89fc-116">*Container (record)*</span></span>

<span data-ttu-id="e89fc-117">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="e89fc-117">The resulting record value.</span></span>

## <a name="example"></a><span data-ttu-id="e89fc-118">Beispiel</span><span class="sxs-lookup"><span data-stu-id="e89fc-118">Example</span></span>

<span data-ttu-id="e89fc-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` gibt den Datencontainer für Anlage **COMP-000001** zurück, der für das Wertmodell **Aktuell** und für einen Zeitraum von **Date1** bis **Date2** vorbereitet wurde.</span><span class="sxs-lookup"><span data-stu-id="e89fc-119">`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returns the data container for fixed asset **COMP-000001** that has been prepared for the **Current** value model and for a period from **Date1** to **Date2**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e89fc-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="e89fc-120">Additional resources</span></span>

[<span data-ttu-id="e89fc-121">Andere (geschäftsdomänenspezifische) Funktionen</span><span class="sxs-lookup"><span data-stu-id="e89fc-121">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]