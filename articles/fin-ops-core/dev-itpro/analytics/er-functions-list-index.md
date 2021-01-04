---
title: INDEX EB-Funktion
description: In diesem Thema werden Informationen zur Verwendung der INDEX-Funktion bei der elektronischen Berichterstellung (EB) bereitgestellt.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a49def8aaa5398fbc7e0f06cc26df8a745207c93
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687990"
---
# <a name="index-er-function"></a><span data-ttu-id="ea290-103">INDEX EB-Funktion</span><span class="sxs-lookup"><span data-stu-id="ea290-103">INDEX ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea290-104">Die Funktion `INDEX` gibt den Wert *Container (Datensatz)* zurück, der unter Verwendung des angegebenen numerischen Index in der angegebenen Liste ausgewählt wird.</span><span class="sxs-lookup"><span data-stu-id="ea290-104">The `INDEX` function returns a *Container (record)* value that is selected by using the specified numeric index in the specified list.</span></span> <span data-ttu-id="ea290-105">Wenn sich der Index außerhalb des Bereichs für die Datensätze in der angegebenen Liste befindet, wird eine Ausnahme ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="ea290-105">If the index is out of range for the records in the specified list, an exception is thrown.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea290-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea290-106">Syntax</span></span>

```vb
INDEX (list, index)
```

## <a name="arguments"></a><span data-ttu-id="ea290-107">Argumente</span><span class="sxs-lookup"><span data-stu-id="ea290-107">Arguments</span></span>

<span data-ttu-id="ea290-108">`list`: *Datensatzliste*</span><span class="sxs-lookup"><span data-stu-id="ea290-108">`list`: *Record list*</span></span>

<span data-ttu-id="ea290-109">Der gültige Pfad einer Datenquelle des Datentyps *Datensatzliste*.</span><span class="sxs-lookup"><span data-stu-id="ea290-109">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="ea290-110">`index`: *Integer*</span><span class="sxs-lookup"><span data-stu-id="ea290-110">`index`: *Integer*</span></span>

<span data-ttu-id="ea290-111">Ein numerischer Index, der die Position des gewünschten Datensatzes in der angegebenen Liste angibt.</span><span class="sxs-lookup"><span data-stu-id="ea290-111">A numeric index that indicates the position of the desired record in the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="ea290-112">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="ea290-112">Return values</span></span>

<span data-ttu-id="ea290-113">*Container (Datensatz)*</span><span class="sxs-lookup"><span data-stu-id="ea290-113">*Container (record)*</span></span>

<span data-ttu-id="ea290-114">Der resultierende Datensatzwert.</span><span class="sxs-lookup"><span data-stu-id="ea290-114">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="ea290-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ea290-115">Example 1</span></span>

<span data-ttu-id="ea290-116">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben und diese den Ausdruck `SPLIT ("A|B|C", "|")` enthält, gibt der Ausdruck `DS.Value` den Textwert **"B"** für den zweiten Datensatz dieser Datensatzliste zurück.</span><span class="sxs-lookup"><span data-stu-id="ea290-116">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `DS.Value` returns the text value **"B"** for the second record of this record list.</span></span> <span data-ttu-id="ea290-117">Der Ausdruck `INDEX (SPLIT ("A|B|C", "|"), 2).Value` gibt auch den Textwert **"B"** zurück.</span><span class="sxs-lookup"><span data-stu-id="ea290-117">The expression `INDEX (SPLIT ("A|B|C", "|"), 2).Value` also returns the text value **"B"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="ea290-118">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ea290-118">Example 2</span></span>

<span data-ttu-id="ea290-119">Wenn Sie die Datenquelle **DS** des Typs *Berechnetes Feld* eingeben, und sie den Ausdruck `SPLIT ("A|B|C", "|")` enthält, löst der Ausdruck `INDEX (SPLIT ("A|B|C", "|"), 4).Value` zur Laufzeit eine Ausnahme aus.</span><span class="sxs-lookup"><span data-stu-id="ea290-119">If you enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A|B|C", "|")`, the expression `INDEX (SPLIT ("A|B|C", "|"), 4).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ea290-120">Zusätzliche Ressourcen</span><span class="sxs-lookup"><span data-stu-id="ea290-120">Additional resources</span></span>

[<span data-ttu-id="ea290-121">Listenfunktionen</span><span class="sxs-lookup"><span data-stu-id="ea290-121">List functions</span></span>](er-functions-category-list.md)
